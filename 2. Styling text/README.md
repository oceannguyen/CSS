## Fundamental text and font styling

- Font styles: Các thuộc tính tác động đến kiểu chữ văn bản, cỡ chữ và đậm hay nghiêng ...
- Text layout styles: Các thuộc tính tác động đến bố cục văn bản như khoảng cách: dòng, từ, ký tự và căn chỉnh vị trí trong content box.

### Fonts

#### Color

Thuộc tính *color* dùng để thiết lập màu cho nội dung element
```css
p {
    color: red;
}
```
#### Font families

Thuộc tính *font-family* dùng để thiết lập kiểu chữ cho elements được chọn.
```css
p {
  font-family: arial;
}
```
Chỉ có một số kiểu chữ là thường xuyên có trên hầu hết các hệ thống, được gọi là **web safe fonts**
| Tên |	Kiểu | Ghi chú |
| --- | --- | --- |
| Arial | sans-serif | It's often considered best practice to also add Helvetica as a preferred alternative to Arial as, although their font faces are almost identical, Helvetica is considered to have a nicer shape, even if Arial is more broadly available. |
| Courier New |	monospace | Some OSes have an alternative (possibly older) version of the Courier New font called Courier. It's considered best practice to use both with Courier New as the preferred alternative. |
| Georgia | serif | |
| Times New Roman |	serif | Some OSes have an alternative (possibly older) version of the Times New Roman font called Times. It's considered best practice to use both with Times New Roman as the preferred alternative. |
| Trebuchet MS | sans-serif | You should be careful with using this font — it isn't widely available on mobile OSes. |
| Verdana | sans-serif	| |

**Font stacks**: Vì ta không thể đảm bảo rằng sự sẵn có của kiểu font muốn áp dụng vào web do vậy bạn có thể chỉ định một **font stack** để trình duyệt có nhiều lựa chọn khi tìm kiểu font.
```css
p {
  font-family: "Trebuchet MS", Verdana, sans-serif;
}
```
> Lưu ý: Kiểu font có chứa khoảng trắng cần đặt trong dấu nháy kép ""

Trong ví dụ trên nếu không có kiểu 'Trebuchet MS' trên máy tính, hệ thống tìm kiểu 'Verdana' trong danh sách và cứ thế cho đến khi tìm được kiểu chỉ định. Trong trường hợp không tìm được kiểu font nào trình duyệt sẽ áp dụng font mặc định là 'Times New Roman'.

#### Font size

Font size có thể được chỉ định các giá trị với hầu các đơn vị đo như đã đề cập ở phần [CSS values and units](), tuy nhiên hầu như ta thường sử dụng các đơn vị sau:

- px: Số pixels muốn đặt cho văn bản. Đây là đơn vị tuyệt đối.
- em: 1em bằng với font-size được đặt cho *parent element*. Đơn vị này trở nên khá phức tạp khi ta có nhiều element lồng nhau với các font-size khác nhau.
- rem: Tương tự như đơn vị *em*, nhưng 1rem bằng với font-size được đặt cho **root element**. Đơn vị khá hữu dụng khi ước lượng tính toán kích thước nhưng có điều trong trình duyệt Internet Explorer 8 và phiên trước không hỗ trợ đợn vị này.
```css
html {
  font-size: 10px;
}

h1 {
  font-size: 2.6rem;
}

p {
  font-size: 1.4rem;
  color: red;
  font-family: Helvetica, Arial, sans-serif;
}
```

#### Font style, font weight, text transform, and text decoration

CSS cung cấp 4 thuộc tính phổ biến để chỉnh *the visual weight/emphasis of text*:
* ```font-style```: Dùng để tắt/bật chế độ chữ nghiêng
    * ```normal```
    * ```italic```
    * ```oblique```
* ```font-weight```: Dùng để chỉnh độ đậm văn bản
    * ```normal```, ```bold```
    * ```lighter```, ```bolder```
    * ```100```-```900```
* ```text-transform```: Dùng để biến đổi văn bản
    * ```none```
    * ```uppercase```
    * ```lowercase```
    * ```capitalize```
    * ```full-width```
* ```text-decoration```: Dùng để trang trí trên fonts (thông thường dùng để bỏ gạch chân khi styling thẻ a)
    * ```none```
    * ```underline```
    * ```overline```
    * ```line-through```

```css
html {
  font-size: 10px;
}

h1 {
  font-size: 2.6rem;
  text-transform: capitalize;
}

h1 + p {
  font-weight: bold;
}

p {
  font-size: 1.4rem;
  color: red;
  font-family: Helvetica, Arial, sans-serif;
}
```

### Text layout

#### Text alignment

Thuộc tính ```text-align``` được dùng để kiểm soát văn bản được căn chỉnh trong content box như thế nào, gồm có các giá trị sau:
* ```left```
* ```right```
* ```center```
* ```justify```

#### Line height

Thuộc tính ```line-height``` dùng để đặt độ cao của mỗi dòng vòng văn bản - với bất kể giá trị nào trong đơn vị đo [CSS values and units](), nhưng khuyến khích dùng giá trị **1.5-2**
```css
line-height: 1.5;
```

#### Letter and word spacing

Thuộc tính ```letter-spacing``` và ```word-spacing``` cho phép ta đặt khoảng cách giữa các ký tự và khoảng cách giữa các từ trong văn bản.
```css
p::first-line {
  letter-spacing: 2px;
  word-spacing: 4px;
}
```

#### [Other properties worth looking at](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals)