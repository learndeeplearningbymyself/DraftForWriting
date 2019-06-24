## Search In Depth

Nguồn:

https://stackoverflow.com/questions/26001002/elasticsearch-difference-between-term-match-phrase-and-query-string

https://www.elastic.co/guide/en/elasticsearch/guide/current/_closer_is_better.html

https://www.elastic.co/guide/en/elasticsearch/guide/current/shingles.html#shingles

### Phân biệt giữa Term, Match Phrase, Query String

**Term** query sẽ match một term đơn mà không đi được **analyzed**, nên giá trị đó không nhất thiết phải **lowercased**.

Ví dụ: Nếu đưa **Bennett** vào ở thời gian index và giá trị không được **analyzed** thì câu query sau sẽ không trả về giá trị gì cả

```
{
  "query": {
    "term" : { "user" : "bennett" }
  }
}
```

**match_phrase** query sẽ analyze input nếu **analyzer** được định nghĩa cho query fields và tìm các documents thoả mãn các tiêu chí sau:

- **Tất cả các terms** phải xuất hiện trong field
- Chúng phải có **cùng thứ tự** như giá trị đầu vào

Ví dụ: nếu chúng ta đánh index cho các documents sau (đánh cho trường **foo** bằng **standard analyzer**)

```
{ "foo": "I just said hello world" }

{ "foo": "Hello world" }

{ "foo": "World Hello" }
```

Câu **match_phrase** query sau đây sẽ chỉ trả về document thứ nhất và thứ 2

```
{
  "query": {
    "match_phrase": {
      "foo": "Hello World"
    }
  }
}
```

### Phrase matching

### Closer is better

Trong khi các câu **phrase queries**  thông thường sẽ loại bỏ đi các documents không bao hàm chính xác phrase trong câu query thì **proximity query** khi mà **slop** lớn hơn 0 - sẽ kết hợp giá trị này trong việc tính giá trị **_score** cuối cùng. Bằng việc thiết lập giá trị cao cho **slop** (50 hoặc 100) sẽ giúp ta loại bỏ đi các documents mà các terms của nó khá xa nhau cũng như đem lại cho các documents thoả mã câu truy vấn có số điểm cao hơn (khi mà các terms có khoảng cách không quá xa nhau)

Câu proximity query sau đây cho cụm **quick dog** match cả hai documents bao gồm các từ **quick** và **dog** nhưng đem lại score cao hơn cho document mà các terms là gần nhau hơn
```
POST /my_index/my_type/_search
{
   "query": {
      "match_phrase": {
         "title": {
            "query": "quick dog",
            "slop":  50 
         }
      }
   }
}
```

Kết quả:
```
{
  "hits": [
     {
        "_id":      "3",
        "_score":   0.75, (1)
        "_source": {
           "title": "The quick brown fox jumps over the quick dog"
        }
     },
     {
        "_id":      "2",
        "_score":   0.28347334, (2)
        "_source": {
           "title": "The quick brown fox jumps over the lazy dog"
        }
     }
  ]
}
```
score của (1) cao hơn (2) là do 2 từ **quick** và **dog** của chúng gần nhau hơn.

### Finding Associated Words

phrase và proximity có thể rất hữu dụng, tuy nhiên nó cung có 1 vài khuyết điểmđiểm. Có thể kể đến như chúng khá nghiêm ngặt trong việc yêu cầu mọi terms phải xuất hiện trong trong câu truy vấn để match, kể cả khi sử dụng **slop**

Việc không quá nghiêm ngặt trong thứ tự của các từ khi sử dụng **slop** có thể dẫn đến việc mất đi tính kết nối giữa các từ này, trong khi chúng ta hoàn toàn có thể đưa ra được documents nào chứ các terms này đủ gần nhau

Việc các từ ghép với các từ khác sẽ tạo nên 1 cụm nhiều ý nghĩa hơn là các từ riêng lẻ. VD: **I’m not happy**, **I’m working**, **I’m happy I’m not working** có thể có cùng các từ thành phần nhưng lại có ý nghĩa hoàn toàn khác nhau

Thay vì index các từ riêng lẻ, ta sẽ index các từ theo cặp (phrase - cụm). Ví dụ với câu **Sue ate the alligator**, ta không chỉ index các từ riêng lẻ (**unigram**) **["sue", "ate", "the", "alligator"]** mà còn index theo cặp (**bigrams** - **shingles**) **["sue ate", "ate the", "the alligator"]**, không chỉ vậy khái niệm **shingles** còn có thể áp dụng cho **trigram** - tức là cụm 3 từ đơn. Việc sử dụng trigram có thể giúp cho độ chính xác cao hơn tuy nhiên nó lại làm tăng thời gian index dữ liệu. Nên đa phần trong nhiều trường hợp sẽ sử dụng bigram là chủ yếu

Một chú ý là **shingles** sẽ không match với các query chứa **sue alligator** mà query trên sẽ match với các từ đơn đã được index

### Producing Shingles

Việc tạo ra shingles sẽ được tiến hành trong quá trình analysis. Thường sẽ giữ cho các unigrams và bigrams riêng biệt để quá trình query là độc lập. Nền tảng của quá trình tìm kiếm vẫn sẽ là unigram trong khi bigram sẽ làm tăng score cho kết quả

```
GET /my_index/my_type/_search
{
   "query": {
      "bool": {
         "must": {
            "match": {
               "title": "the hungry alligator ate sue"
            }
         },
         "should": {
            "match": {
               "title.shingles": "the hungry alligator ate sue"
            }
         }
      }
   }
}
```
Câu query trên có nghĩa là phải **match với tokenizer trước** rồi mới match với shingles

Cách tính score với **shingle**: Nếu có tokenizer thì tính điểm bằng cách cộng hết điểm của tất cả tokenizers / document, tất cả shingles / document, còn nếu ko có tokenizer thì ko tính nữa.
