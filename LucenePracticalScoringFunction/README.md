## Lucence's Practical Scoring Function

Bài viết được dịch từ: https://www.elastic.co/guide/en/elasticsearch/guide/current/practical-scoring-function.html

Với truy vấn multiterm, Lucence lấy **Boolean model**, TF/IDF và **vector space model** và kết hợp chúng lại trong một package - package này sẽ là tập các matching documents cùng score của chúng

Xét ví dụ:

Câu truy vấn:

```
GET /my_index/doc/_search
{
  "query": {
    "match": {
      "text": "quick fox"
    }
  }
}
```

sẽ được viết lại như sau:

```
GET /my_index/doc/_search
{
  "query": {
    "bool": {
      "should": [
        {"term": { "text": "quick" }},
        {"term": { "text": "fox"   }}
      ]
    }
  }
}
```

**Bool query** sẽ triển khai **Boolean model** và trong ví dụ này, sẽ chỉ bao gồm các documents chứa hoặc là term **quick** hoặc **fox** hoặc cả hai.

Ngay khi mà document math với query. Lucence sẽ tính score của document đó tương ứng với query (bao gồm việc kết hợp scores của mỗi matching term). Công thức sử dụng để tính toán score gọi là **practical scoring function**. Tuy nhìn phức tạp nhưng không thể bỏ qua. Dưới đây là công thức

```
score(q,d)  =  
        queryNorm(q)  
        · coord(q,d)    
        · ∑ (           
            tf(t in d)   
            · idf(t)²      
            · t.getBoost() 
            · norm(t,d)    
        ) (t in q)

score(q, d): là relevance score của document d với query q
queryNorm(q): là query norm (sẽ được trình bày dưới đây)
coord(q, d): coordinator (hiểu nôm nà là toạ độ)
tf(t in d): term frequency của term t trong document d
idf(t): inverse document frequency của term t
t.getBoost(): boost được áp dụng cho truy vấn
norm(t, d): field-length norm, kết hợp với index-time field-level boost
```

### Query Normalization



