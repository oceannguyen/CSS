# Web fonts

Cho phép bạn tải các custom fonts đi cùng với trang web của bạn, cho đa dạng font hơn so với các web safe fonts.

Đầu tiên bạn có một khối ```@font-face``` đặt trên cùng CSS

```css
@font-face {
  font-family: "myFont";
  src: url("myFont.ttf");
}
```

Sau đó bạn có thể chỉ định tên font-family được chỉ định trong @font-face để áp dụng lên bất cứ đâu bạn muốn:

```css
html {
  font-family: "myFont", "Bitstream Vera Serif", serif;
}
```

Có 2 điểm quan trọng cần nhớ về web fonts là:

* Các trình duyệt hỗ trợ các định dạnh font khác nhau, bạn cần nhiều định dạng font để hỗ trợ trình duyệt.

* Fonts thường không miễn phí.

## Sinh định dạng font cho trình duyệt như thế nào

* Bước 1: Tìm một loại font nào đó

* Bước 2: Sử dụng tool ví dụ như [Font Squirrel](https://www.fontsquirrel.com/tools/webfont-generator) để sinh định dạng khác nhau cho font của bạn

* Bước 3: Sau khi tải định dạng đã được sinh ra, bạn định nghĩa @font-face cho loại font đó với các loại format khác nhau.

## Sử dụng Online Font Service

Các dịch vụ font online để lưu trữ và phục vụ các fonts cho bạn. Vì vậy bạn không cần phải lo lắng về việc viết code cho ```@font-face```, chỉ insert 1/2 dòng code vào trang của bạn là đủ. 

Hầu hết các dịch vụ font online như vậy đều phải đăng ký, ngoại trừ các fonts của [Google fonts](https://fonts.google.com/) hoàn toàn miễn phí.

### Các bước để thêm font service

* Truy cập [Google fonts](https://fonts.google.com/)
* Chọn font mà bạn muốn
* Sau đó nhấn *[Number] Families Selected* ở phía dưới trang
* Trên màn hình hiển thị HTML code, copy thẻ ```<link>``` và chèn vào trang HTML của bạn
* Tiếp theo copy đoạn CSS cho ```font-family``` vào CSS mà bạn muốn.