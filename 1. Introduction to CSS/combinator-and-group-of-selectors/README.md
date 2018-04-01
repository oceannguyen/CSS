## Combinators and Groups of selectors

Việc chọn một element đôi khi không hiệu quả. CSS có một vài cách để chọn elements dựa trên việc chúng có quan hệ/liên kết với nhau như thế nào.

Combinators các bộ theo mối quan hệ của chúng, ví dụ với A và B là 2 bộ chọn bất kỳ:
- A, B: Bất cứ elements nào thuộc bộ chọn A/Bất
- A B: Chọn elements có bộ chọn B và trước đó có cha là A
- A > B: Chọn elements có bộ chọn B và có A là cha trực tiếp
- A + B: Chọn elements có bộ chọn B mà kế tiếp bộ chọn A
- A ~ B: Chọn elements có bộ chọn B mà sau bộ chọn A

Groups các bộ chọn vào thành một tập quy tắc (the rule)