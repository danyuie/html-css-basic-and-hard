# What is Hyper Text Markup Language (HTML) ?
<br />
<aside>
👩‍💻 HTML là ngôn ngữ đánh dấu xác định cấu trúc nội dung của bạn. HTML bao gồm một loạt các phần tử mà bạn sử dụng để bao bọc hoặc bao bọc các phần khác nhau của nội dung nhằm làm cho nội dung đó xuất hiện theo một cách nhất định hoặc hoạt động theo một cách nhất định. Các thẻ kèm theo có thể tạo siêu liên kết từ hoặc hình ảnh đến một nơi khác, có thể in nghiêng các từ, có thể làm cho phông chữ lớn hơn hoặc nhỏ hơn, v.v.
</aside>
<br />
<br />

# **# PHẦN TỬ TRONG HTML**

<br />

```html
<p>My cat is very grumpy</p>
```

![https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-small.png](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-small.png)

<br />

**Các phần chính của đoạn mã trên:**

1. **Thẻ mở:** Thẻ này bao gồm tên của phần tử (trong trường hợp này là p), được gói trong **dấu ngoặc nhọn** mở và đóng . Điều này cho biết nơi phần tử bắt đầu hoặc bắt đầu có hiệu lực
2. **Thẻ đóng:** Thẻ này giống như thẻ mở, ngoại trừ việc nó có **dấu gạch chéo** lên trước tên thành phần. Điều này cho biết nơi phần tử kết thúc. Không thêm thẻ đóng là một trong những lỗi cơ bản của người mới bắt đầu và có thể dẫn đến kết quả lạ.
3. **Nội dung:** Đây là nội dung của phần tử, trong trường hợp này chỉ là văn bản.
4. **Phần tử:** Thẻ mở, thẻ đóng và nội dung cùng nhau tạo thành phần tử.

<br />

**Các phần tử cũng có thể có các thuộc tính giống như sau:**

```html
<p class='editor-note'>My cat is very grumpy</p>
```

![https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-attribute-small.png](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-attribute-small.png)

Thuộc tính chứa thông tin bổ sung về thành phần mà bạn không muốn xuất hiện trong nội dung thực tế. Ở đây, **`class`** là tên thuộc tính và **`editor-note`** là giá trị thuộc tính . Thuộc tính **`class`** này cho phép bạn cung cấp cho phần tử một mã định danh không duy nhất có thể được sử dụng để nhắm mục tiêu đến phần tử đó (và bất kỳ phần tử nào khác có cùng **`class`** giá trị) với thông tin về kiểu dáng và những thứ khác. Một số thuộc tính không có giá trị, chẳng hạn như **`required`.**

**Các thuộc tính đặt giá trị luôn có:**

1. Khoảng trắng giữa nó và tên phần tử (hoặc thuộc tính trước đó, nếu phần tử đã có một hoặc nhiều thuộc tính). 
2. Tên thuộc tính theo sau là **dấu bằng**. 
3. Giá trị thuộc tính được bao bọc bởi **dấu ngoặc kép mở và đóng**.

> ***Lưu ý:** Các giá trị thuộc tính đơn giản không chứa khoảng trắng ASCII (hoặc bất kỳ ký tự nào " ' ` = < >) có thể không được trích dẫn, nhưng bạn nên trích dẫn tất cả các giá trị thuộc tính vì nó làm cho mã nhất quán và dễ hiểu hơn.*
> 

<br />

# **# PHẦN TỬ LỒNG NHAU**

<br />

Bạn cũng có thể đặt các phần tử bên trong các phần tử khác - điều này được gọi là **lồng nhau.**

```html
<p class='editor-note'>My cat is <strong>very</strong> grumpy</p>
```

Tuy nhiên, bạn cần đảm bảo rằng các phần tử của bạn được lồng đúng cách. Trong ví dụ trên, chúng ta mở `**<p>**` phần tử trước, sau đó là `**<strong>**` phần tử; do đó, chúng ta phải đóng **`<strong>`** phần tử trước, sau đó là **`<p>`** phần tử. Sau đây là không chính xác:

```html
<p class='editor-note'>My cat is <strong>very grumpy</p></strong>
```

Các phần tử phải mở và đóng chính xác để chúng rõ ràng ở bên trong hoặc bên ngoài nhau. Nếu chúng trùng nhau như minh họa ở trên thì trình duyệt web của bạn sẽ cố gắng đưa ra dự đoán chính xác nhất về những gì bạn đang muốn nói, điều này có thể dẫn đến kết quả không mong muốn. Vì vậy đừng làm điều đó!

<br />

# **# PHẦN TỬ TRỐNG**

<br />

Một số phần tử không có nội dung và được gọi là **void element**. Lấy ví dụ phần tử <img> phần tử mà chúng ta đã có trong trang HTML của mình:

```html
<img src="images/firefox-icon.png" alt="My test image" />
```

Cái này chứa hai thuộc tính, nhưng không có **`</img>`** thẻ đóng và không có nội dung bên trong. Điều này là do phần tử hình ảnh không bao bọc nội dung để ảnh hưởng đến nó. Mục đích của nó là nhúng một hình ảnh vào trang HTML ở vị trí nó xuất hiện.

<br />

# **# CÁC PHẦN TỬ THÔNG DỤNG TRONG HTML**

<br />

## 1. Cơ Bản
| Tag | Mô tả |
| --- | --- |
| <!DOCTYPE> |      Xác định cho trình duyệt biết phiên bản HTML mà bạn đang sử dụng |
| ```<html>``` |      Xác định một tài liệu HTML |
| ```<head>``` |      Xác định phần đầu của tài liệu HTML (chứa các thẻ cung cấp thông tin cho trang web) |
| ```<body> ``` |       Xác định phần thân của tài liệu HTML (chứa những phần tử sẽ được hiển thị lên màn hình) |
| ```<h1> ``` → ```<h6> ``` |       Tạo những đề mục quan trọng trong trang web |
| ```<p> ``` |      Xác định một đoạn văn bản |
| ```<br> ``` |       Chèn một ngắt xuống dòng |
| ```<hr> ``` |       Tạo một đường kẻ phân cách nằm ngang |
| >```<!-- -- ``` |       Xác định một đoạn chú thích (chứa những phần tử sẽ KHÔNG được hiển thị lên màn hình) |

## 2. ****Formatting****
| Tag | Mô tả |
| --- | --- |
| ```<style>``` | Dùng để làm thùng chứa cho các đoạn mã CSS |
| ```<div>``` | Nhóm các phần tử lại với nhau để tiện cho việc thiết kế bố cục của trang web |
| ```<span>``` | Nhóm các phần tử nội tuyến lại với nhau để tiện cho việc định dạng CSS |
| ```<a>``` | Tạo một liên kết đến một tài liệu nào đó (khi người dùng bấm vào liên kết thì sẽ được chuyển đến tài liệu đó) |
| ```<main>``` | Xác định phần thân của trang web |
| ```<header>``` | Xác định phần đầu của trang web |
| ```<footer>``` | Xác định phần chân của trang web |

## 3. Lists
| Tag | Mô tả |
| --- | --- |
| ```<ul>``` | Xác định một danh sách không có thứ tự |
| ```<ol>``` | Xác định một danh sách có thứ tự |
| ```<li>``` | Xác định một "danh mục" trong danh sách |

## 4. ****Tables****
| Tag | Mô tả |
| --- | --- |
| ```<table>``` | Xác định phần tử là một cái bảng |
| ```<caption>``` | Tạo tiêu đề cho bảng |
| ```<th>``` | Xác định phần tử là một ô tiêu đề trong hàng |
| ```tr>``` | Xác định phần tử là một hàng trong bảng |
| ```<td>``` | Xác định phần tử là một ô trong hàng |
| ```<thead>``` | Xác định những dòng nào thuộc "phần đầu" của bảng |
| ```<tbody>``` | Xác định những dòng nào thuộc "phần thân" của bảng |
|```<tfoot>``` | Xác định những dòng nào thuộc "phần chân" của bảng |

<br />

# **# MỘT TÀI LIỆU HTML HOÀN CHỈNH SẼ NTN?**

<br />

```html
<!doctype html>
<html lang="en-US">
	
	<!--** đây là phần đầu của tài liệu - phần này sẽ không được in ra trình duyệt **-->
	<!--** Mục đích là để khai báo các thông tin cho trình duyệt xử lý **-->
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>My test page</title>
  </head>
	
	<!--** đây là phần thân của tài liệu - phần này sẽ in ra trình duyệt **-->
  <body>
    <img src="images/firefox-icon.png" alt="My test image" />
  </body>
	
</html>
```