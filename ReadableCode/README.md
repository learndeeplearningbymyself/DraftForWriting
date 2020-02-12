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

```javascript
// This class is getting messy. Maybe we should create a 'ResourceNode' subclass to
// help organize things.
```

Đoạn comment trên không chỉ cho thấy code hiện tại đang khá "tồi" mà còn chỉ cho người đọc kế tiếp về cách sửa, khiến cho người đọc không bị "hoảng" và không dám "động vào" đoạn code đó.

#### Comment the Flaws in Your Code

Không đoạn code nào là không có lỗ hổng nếu xét về tính dài hạn, vậy nên đừng xấu hổ nếu comment rằng:
- Cần cải thiện đoạn code này trong tương lai
- Giải thuật hiện tại chưa tốt
- ...

Những comments như vậy không những giúp cho code của bạn có thể sẽ được cải thiện trong tương lai mà còn giúp người đọc có một cái nhìn cụ thể hơn về chất lương của code

Sẽ có các quy ước khác nhau giữa dev về việc tạo ra các "markers" kiểu này. Ví dụ như

- TODO: việc cần làm trong tương lai
- FIX-ME: cho biết có lỗi ở đoạn code hiện tại
- XXX: Dầu hiệu cho thấy có thể có lỗi nghiêm trọng
- HACK: Thừa nhận về giải pháp tồi cho vấn đề hiện tại

#### Comment on Your Constants

Sau mỗi constant đều là một "câu chuyện" về mục đích cũng như ý nghĩa của nó. Ví dụ như sau:

```python
NUM_THREADS = 8;
```

Có lẽ người viết code sẽ nghĩ rằng, không cần comment cho constant này làm gì vì bản thân tên gọi của nó đã nói lên tất cả. Thế nhưng những người đọc code lại thích comment hơn:

```python
NUM_THREADS = 8 # as long as it's >= 2 * num_processors, that's good enough.
```

Việc comment sẽ giúp người đọc code có thể biết được cách điều chỉnh giá trị của hằng số sao cho phù hợp. Đôi khi các giá trị hằng số là ước lượng

```C
// Impose a reasonable limit - no human can read that much anyway.
   const int MAX_RSS_SUBSCRIPTIONS = 1000;
```

Hoặc là những giá trị "highly tuned" - các giá trị này không nên bị chỉnh sửa

```C
image_quality = 0.72; // users thought 0.72 gave the best size/quality tradeoff
```

Với hằng số dạng `SECONDS_PER_DAY` thì không cần comment vì bản thân tên của hằng số cũng đã nói lên ý nghĩa của nó.

#### Put Yourself in the Reader’s Shoes

Kĩ thuật sử dụng trong cuốn sách này để cấu thành nên nội dung chính đó là "Đặt mình vào vị trí của người đọc code" để từ đó biết được họ cần những thông tin gì để có thể đưa ra comment phù hợp nhất


