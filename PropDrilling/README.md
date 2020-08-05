# Prop Drilling

※ Bài viết được dịch từ nguồn: https://kentcdodds.com/blog/prop-drilling

*Prop Drilling là gì, tại sao nó lại có những ưu điểm cũng như những nhược điểm, và làm thế nào để tránh được các vấn đề thường gặp với nó*

Mục tiêu của bài viết này không chỉ giúp bạn hiểu rõ prop drilling là gì (prop drilling còn được gọi với tên khác là "threading") mà còn giúp bạn có thể tránh được các vấn đề thường gặp với nó.

## Prop Drilling là gì?

Prop drilling (còn được gọi là "threading") là thuật ngữ chỉ tiến trình mà bạn phải đi qua để có thể lấy dữ liệu cho các phần của React component tree. Cùng quan sát một ví dụ đơn giản với "stateful component"
