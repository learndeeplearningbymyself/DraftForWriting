## ElasticSearch Slop

Bài viết được dịch từ nguồn - https://www.elastic.co/guide/en/elasticsearch/guide/current/slop.html

### Mixing it up
Việc yêu cầu match các phrase một cách chính xác là một điều kiện khá khó. Chúng ta muốn rằng các documents bao hàm cụm **quick brown fox** cũng được xem xét là match với câu truy vấn **quick fox** kể cả khi vị trí là không chính xác tuyệt đối.

Chúng ta có thể xem xét một mức độ linh hoạt về việc matching phrase bằng việc sử dụng **slop paramter**

```
GET /my_index/my_type/_search
{
    "query": {
        "match_phrase": {
            "title": {
                "query": "quick fox",
                "slop":  1
            }
        }
    }
}
```
**slop paramter** sẽ cho **match_phrase query** biết mức độ đối ta mà term vẫn được xem xét là match với document. Mức độ tối đa ở đây có nghĩa là **Chúng ta cần di chuyển 1 term bao nhiêu lần để khiến cho query và document vẫn match** 

Ta xét một ví dụ đơn giản như sau: Để khiến cho query **quick fox** match mới document chứa cụm **quick brown fox** ta cần **slop = 1**

```
            Pos 1         Pos 2         Pos 3
-----------------------------------------------
Doc:        quick         brown         fox
-----------------------------------------------
Query:      quick         fox
Slop 1:     quick                 ↳     fox
```

Mặc dù tất cả các từ cần phải có trong **phrase matching** kể cả khi sử dụng **slop**, các từ không nhất thiết cần phải theo đúng như thứ tự để match. Với giá trị **slop** đủ lớn, các từ có thể được sắp xếp theo bất kì thứ tự nào

Để làm cho query **fox quick** ta cần **slop = 3**
```
            Pos 1         Pos 2         Pos 3
-----------------------------------------------
Doc:        quick         brown         fox
-----------------------------------------------
Query:      fox           quick
Slop 1:     fox|quick  ↵  (1)
Slop 2:     quick      ↳  fox
Slop 3:     quick                 ↳     fox
```

Chú ý rằng **fox** và **quick** ở cùng vị trí trong bước (1). Thay đổi vị trí **fox quick** thành **quick fox** yêu cầu **slop = 2**
