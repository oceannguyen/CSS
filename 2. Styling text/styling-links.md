# Styling links

Khi styling **links**, điều quan trọng cần nắm là các sử dụng psuedo-classes để style các trạng thái links hiệu quả.

## Các trạng thái của link

Link có 5 trạng thái là:

* **Link**: Trạng thái ban đầu. Sử dụng psuedo-class ```:link``` để style
* **Visited**: Link khi đã ghé thăm. Sử dụng psuedo-class ```:visited``` để style
* **Hover**: Khi hover qua link. Sử dụng psuedo-class ```:hover``` để style
* **Focus**: Khi link được trỏ đến bằng phím tab. Sử dụng psuedo-class ```:focus``` để style
* **Active**: Khi được nhấn/giữ. Sử dụng psuedo-class ```:active``` để style

```css
// Example

a {
  outline: none;
  text-decoration: none;
  padding: 2px 1px 0;
}

a:link {
  color: #265301;
}

a:visited {
  color: #437A16;
}

a:focus {
  border-bottom: 1px solid;
  background: #BAE498;
}

a:hover {
  border-bottom: 1px solid;     
  background: #CDFEAA;
}

a:active {
  background: #265301;
  color: #CDFEAA;
}
```

```html
<p>There are several browsers available, such as <a href="#">Mozilla
Firefox</a>, <a href="#">Google Chrome</a>, and
<a href="#">Microsoft Edge</a>.</p>
```

> **Thuộc tính ```outline``` thường được chỉ định với giá trị là ```none``` bởi vì các trình duyệt hiển thị thuộc tính khác nhau.**

## [Gắn thêm icon vào link như thế nào](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Styling_links)

## [Example styling links as buttons](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Styling_links)

## [Loại bỏ khoảng trắng giữa các inline-block elements](https://css-tricks.com/fighting-the-space-between-inline-block-elements/)
