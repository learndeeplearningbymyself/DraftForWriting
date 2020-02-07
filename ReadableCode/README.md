## Bản dịch và tóm tắt bằng tiếng Việt nội dung cuốn sách Readable Code

Ta xét ví dụ đoạn code sau

```python
# remove everything after the second '*'
name = '*'.join(line.split('*')[:2])
```

Thực sự comment ở đây là không cần thiết vì nó không hề cung cấp bất kì thông tin mới nào cho người đọc cả. Tuy nhiên trong thực tế đa phần các dev sẽ đọc comment để nắm nội dung đoạn code nhanh hơn mà không cần phải đọc code

#### Don’t Comment Just for the Sake of Commenting

Khi thực hiện các bài tập về lập trình, chúng ta thường được yêu cầu về việc viết comment cho các hàm mình đã viết. Điều này đôi khi khiến chúng ta chỉ comment một cách "chống đối" như ví dụ dưới đây

```C
// Find the Node in the given subtree, with the given name, using the given depth.
Node* FindNodeInSubtree(Node* subtree, string name, int depth);
```

Comment kiểu như trên sẽ bị liệt vào loại "comment vô nghĩa", "vô nghĩa" ở đây nghĩa là comment và code gần như giống nhau, và comment không cung cấp thông tin gì mới hay cụ thể cho người đọc

Nếu muốn comment, hãy cung cấp thêm thông tin chi tiết hơn

```C
// Find a Node with the given 'name' or return NULL.
// If depth <= 0, only 'subtree' is inspected.
// If depth == N, only 'subtree' and N levels below are inspected.
Node* FindNodeInSubtree(Node* subtree, string name, int depth);
```

#### Don’t Comment Bad Names—Fix the Names Instead

Comment không giúp chữa được những cái tên tồi "bad-name", thay vào đó hãy đặt một cái tên "self-documenting" vì cái tên đó sẽ xuất hiện ở nhiều nơi trong project của chúng ta hơn là comment của nó

Ví dụ-1: 

Bad name: "CleanReply", đa phần comment chỉ để giải thích "clean" là như thế nào

```C
// Enforce limits on the Reply as stated in the Request,
// such as the number of items returned, or total byte size, etc.
void CleanReply(Request request, Reply reply);
```

Good name: "EnforceLimitsFromRequest"

```C
// Make sure 'reply' meets the count/byte/etc. limits from the 'request'
void EnforceLimitsFromRequest(Request request, Reply reply);
```

Ví dụ-2:

```C
// Releases the handle for this key. This doesn't modify the actual registry.
void DeleteRegistry(RegistryKey* key);
```

Cái tên **DeleteRegistry** nghe thật là nguy hiểm, thể nhưng comment đã phần nào đó "trấn an" người đọc, vậy tại sao không lựa chọn một cái tên "self-documenting" hơn

```C
void ReleaseRegistryHandle(RegistryKey* key);
```

Tổng quát lên chúng ta sẽ có 1 rule như sau

> good code > bad code + good comments

### Recording Your Thoughts

Vậy chúng ta nên comment như thế nào. Các "comment tốt" sẽ là công cụ để "ghi lại suy nghĩ, ý tưởng của bạn" khi đang tiến hành viết code

#### Include “Director Commentary”

Hãy thêm các comments để ghi lại cách nghĩ (insights) mà bạn đưa vào trong code

Ví dụ-1:
```javascript
// Surprisingly, a binary tree was 40% faster than a hash table for this data.
// The cost of computing a hash was more than the left/right comparisons.
```

Comment này cho người đọc biết rằng, không cần phải lãng phí thời gian cho việc tối ưu hoá hiệu năng của code nữa.

Ví dụ-2:
```javascript
// This heuristic might miss a few words. That's OK; solving this 100% is hard.
```

Nếu không có comment này, dev có thể sẽ tốn thời gian cho việc fix bug nếu test case không pass.






