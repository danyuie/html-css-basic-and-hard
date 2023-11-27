# **SASS/SCSS là gì?**

## **1. SASS/SCSS là gì?**

**SASS/SCSS** là một chương trình tiền xử lý CSS (CSS preprocessor). Nó giúp bạn viết CSS theo cách của một ngôn ngữ lập trình, có cấu trúc rõ ràng, rành mạch, dễ phát triển và bảo trì code hơn. Ngoài ra nó có rất nhiều các thư viện hỗ trợ kèm theo giúp bạn viết code CSS một cách dễ dàng vào đơn giản hơn. Có rất nhiều loại CSS Preprocessor trong đó bao gồm SASS, Stylus hay LESS.

> [!NOTE]
> **SASS** và **SCSS** về bản chất vấn đề là giống nhau, chỉ khác nhau ở cách viết 

**SASS** bản thân có hai kiểu viết khác nhau, một kiểu như là **HAML**, **Pug** – Sử dụng indent *(cách thụt đầu dòng)* để phân tách các khối code , sử dụng xuống dòng để phân biệt rules , có phần mở rộng là `.sass`. 
```css
.header
  color: #f3f3f3;

.header__inner
  border: 1px solid #f3f3f3
```

**SCSS** sử dụng cú pháp giống với **Ruby** *(vì đơn giản nó được thiết kế bởi các lập trình viên Ruby)*. Có phần mở rộng là `.scss` , **SCSS** ra đời sau **SASS** và có cú pháp viết tương tự như cách viết **CSS**. Cú pháp này được tạo ra nhằm thu hẹp khoảng cách giữa **SASS** và **CSS** bằng cách mang lại một thứ gì đó thân thiện với **CSS**.

## **2 .Các tính năng cơ bản của SCSS**

**a. Xếp chồng – Nested Rules** 

Đây là một tính năng rất hay của SCSS và được sử dụng rất thường xuyên.

Ví dụ nếu bạn chỉ muốn **CSS** cho thẻ `ul` với class menu, với **CSS** thuần bạn sẽ viết:

```css
.navbar ul.menu {
    list-style: none;
}
```

Nếu bạn tiếp tục muốn **CSS** cho thẻ `li` trong thẻ `ul` (có class là menu) thì

```css
.navbar ul.menu li {
    padding: 3px;
}
```

Sau đó bạn muốn tiếp tục **CSS** cho thẻ a trong thẻ `li`,… bạn sẽ phải lặp đi lặp lại tên tag (hoặc `class`, hoặc `id`) cha của thẻ muốn **CSS** thì sẽ rất mệt và nhàm chán. Thay vào đó bạn có thể dùng ***Nested Ruled*** của **SASS** để giúp mọi thứ trở nên đơn giản hơn một cách rõ rệt. Ví dụ:

```css
.navbar {
    ul.menu {
        list-style: none;

        li {
            padding: 3px;

            a {
                text-decoration: none;
            }
        }
    }
}
```

Và sau khi được đoạn **SASS** trên được compile ra **CSS** thuần sẽ như sau:

```css
.navbar ul.menu {
    list-style: none;
}
.navbar ul.menu li {
    padding: 3px;
}
.navbar ul.menu li a {
    text-decoration: none;
}
```

**b. Biến – variable**

Sử dụng biến với **SCSS** vô cùng cơ bản, bạn chỉ cần đặt tên cho biến – bắt đầu bằng `$`. Biến chứa đựng các giá trị mà chúng ta dùng nhiều lần ví dụ như mã màu, font hay kiểu chữ.

```scss
$RedColor = #fff;

.navbar {
    ul.menu {
        list-style: none;

        li {
            padding: 3px;

            a {
                text-decoration: none;
                color: $Redcolor
            }
        }
    }
}
```

**c. Quy tắc Mixin**

**Mixin** giúp bạn tạo các hàm được sử dụng trong **SCSS**, bạn hoàn toàn có thể truyền các tham số vào bên trong nó để sử dụng.

**Mixin** là một cơ chế khá phổ biến trong **SASS**. Công dụng của nó là mang nhiều thuộc tính mà bạn đã quy ước trong một mix nào đó rồi `@include` vào một thành phần bất kỳ mà không cần phải viết lại các thuộc tính đó (Ví dụ ở trên là `color` vs `font-style`)

```scss
@mixin colorVsStyle {
    color: #f06;
    font-style: italic;
}

.navbar {
    ul.menu {
        list-style: none;

        li {
            padding: 5px;

            a {
                text-decoration: none;
                @include colorVsStyle;
            }
        }
    }
}
```

Hoặc nếu bạn không muốn `color` lúc nào cũng là `#f06`, thì bạn có thể truyền thuộc tính vào mix như 1 tham số bằng cách viết như sau:

```scss
@mixin colorVsStyle($color, $fontStyle) {
    color: $color;
    font-style: $fontStyle;
}

.navbar {
    ul.menu {
        list-style: none;

        li {
            padding: 5px;

            a {
                text-decoration: none;
                @include colorVsStyle(#000, italic);
            }
        }
    }
}
```

**d. Kế thừa – Extends**

Khi nghe đến extends hay còn gọi là kế thừa, thì có thể bạn sẽ nghĩ ngay đến OOP (lập trình hướng đối tượng) đúng không? Cách làm sẽ là bạn định nghĩa ra 1 class, rồi những tag nào cần thì `@extend` nó vào là xong:

```scss
.title-box {
    color: ##2EFEC8;
    text-shadow: 0px 0px 10px #6E6E6E;
    display: inline-block;
    text-transform: uppercase;
}

.navbar {
    ul.menu {
        list-style: none;

        li {
            padding: 4px;

            a {
                text-decoration: none;
                @extend .title-box;
            }
        }
    }
}
```

**e. Nhập – Import**

Cú pháp import của **SASS** rất hữu dụng và thường xuyên được sử dụng trong các project. Nó tương tự cách bạn `require` hay `include` file này vào file khác trong **PHP**.

Đặt trường hợp bạn có 1 trang **index**, bao gồm **header**, **body**, **footer**. Thay vì sử dụng **CSS** cho những cái trên vào một `style.css` thì với **SASS** bạn sẽ thực hiện như sau, nhớ có dấu `_` trước tên file được import:

1. Tạo 1 file `_header.scss` để **CSS** riêng cho header.
1. `_body.scss` để **CSS** riêng cho body.
1. `_footer.scss` để **CSS** riêng cho footer.
1. Rồi ở file `style.scss` ta chỉ cần `@import` 3 file trên là mượt mà ngay

file `_header.scss`
```scss
#header {
    // viết code sass ở đây
}
```

file `_body_.scss`
```scss
#body {
    // viết code sass ở đây
}
```

file `_footer_.scss`
```scss
#footer {
    // viết code sass ở đây
}
```

file `style.scss`
```scss
@import 'header';
@import 'body';
@import 'footer';

// viết code sass ở đây
```



## **3. cài đặt sass**
- Cài đặt `Sass` 
    - Nếu bạn chưa cài môi trường cho `Sass` thì tải `Node.js` - [**Download**](https://nodejs.org/en/download/)

    - Install `Sass` bằng `NPM`

        ```
        npm i -g sass
        ```
- Chạy `Sass`
    - Output là file minify có dạng `app.min.css`

        ```
        sass --watch app.sass:../css/app.min.css --style compressed
        ```
        *file `app.min.css` sẽ ở trong thư mục `./assets/css`*
    
    - Output là file css có dạng `app.css`

        ```
        sass --watch app.sass:../css/app.css
        ```
        *file `app.css` sẽ ở trong thư mục `./assets/css`*

## **4. Cây Thư Mục**

    ```
    └───name-project
        ├───assets
            ├───js
            ├───font
            ├───svg
            ├───images
            ├───css
                ├───app.css
                ├───app.min.css
            └───sass
                ├───base
                    ├───_all.sass
                    ├───_mixin.sass
                    ├───_reset.sass
                    ├───_variables.sass
                ├───layout
                    ├───_all.sass
                    ├───_footer.sass
                    ├───_header.sass
                ├───components
                    ├───_all.sass
                    ├───_button.sass
                ├───pages
                    ├───_all.sass
                    ├───_contact.sass
        └───index.html
    ```