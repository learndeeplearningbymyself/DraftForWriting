Elastic Search Practice guide

**2.1. Concepts cơ bản**

- Đơn vị lưu trữ cơ bản là **document** ~= **record** trong **table**, nhưng lưu dưới dạng JSON
Khi đưa vào ElasticSearch các document đều được thêm 1 trường để quản lí đó là **ID**
- Dưới document là **field** - tương đương 1 cặp **key - value**

Khi tiến hành search bằng ElasticSearch đa phần đều search trên field, quá trình index cũng diễn ra trên field

- Kiểu dữ liệu **text** khi lưu trữ sẽ đươc cho đi qua bộ **Analyzer** để tách thành các **tokenizer**
- Kiểu dữ liệu **keyword** thì không bị tokenize mà sẽ được giữ nguyên và tìm kiếm theo *nguyên khối*. VD:

> taro.yamada@example.com

sẽ không bị tìm kiếm theo từng thành phần như **yamada** hay **example.com** mà sẽ là cả khối **taro.yamada@example.com**