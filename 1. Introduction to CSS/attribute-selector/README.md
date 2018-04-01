# Attribute selectors

Bộ chọn thuộc tính là một kiểu chọn đặc biệt dựa trên thuộc tính của elements, được biểu diễn qua dấu ngoặc vuông [].
Attribute selectors được chia làm 2 loại: **Presence and value** và **Substring value**

## Presence and value attribute selectors
- [attr]: Chọn các elements mà có thuộc tính là *attr* bất kể giá vị của nó là gì.
- [attr=val]: Chọn các elements mà có là thuộc tính là *attr* và có giá trị là *val*.
- [attr~=val]: Chọn các elements mà có là thuộc tính là *attr* và có chứa giá trị là *val*. Ví dụ như
```html,css
<li data-quantity="700g" data-vegetable="not spicy like chili">Red pepper</li>

[data-vegetable~="spicy"] {
  color: red;
}
```

Substring value attribute selectors

Được ví như chọn theo biểu thức chính quy