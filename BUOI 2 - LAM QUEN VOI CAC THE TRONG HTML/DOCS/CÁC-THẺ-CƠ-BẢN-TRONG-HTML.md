# **CÁC THẺ CƠ BẢN TRONG HTML VÀ CSS**
<br>

## **1 .Các thẻ cơ bản trong HTML**
<br>

**Thẻ tiêu đề (Heading):** Thẻ tiêu đề được sử dụng để tạo các tiêu đề cho trang web. Có 6 cấp độ tiêu đề, từ `h1` (lớn nhất) đến `h6` (nhỏ nhất).
  ```html
    <h1>Tiêu đề trang</h1>
    <h2>Tiêu đề phụ</h2>
    <h3>Tiêu đề thứ ba</h3>
  ```
<br>  

**Thẻ đoạn văn (Paragraph):** Thẻ đoạn văn được sử dụng để tạo các đoạn văn trên trang web.
```html
  <p>Đây là một đoạn văn.</p>
  <p>Đây là một đoạn văn khác.</p>
```
<br>

**Thẻ hình ảnh (Image):** Thẻ hình ảnh được sử dụng để chèn hình ảnh vào trang web.
```html
  <img src="image.jpg" alt="Ảnh minh họa" width="500" height="300">
```
Trong ví dụ này, thuộc tính `src` được sử dụng để chỉ định đường dẫn đến hình ảnh, thuộc tính `alt` được sử dụng để cung cấp một mô tả ngắn gọn cho hình ảnh trong trường hợp hình ảnh không tải được, và thuộc tính `width` và `height` được sử dụng để đặt kích thước của hình ảnh.

<br>

**Thẻ liên kết (Anchor):** Thẻ liên kết được sử dụng để tạo các liên kết đến các trang web khác hoặc các phần khác của cùng một trang web.

```html
  <a href="https://example.com" target="_blank">Liên kết đến trang web khác</a>
```
Trong ví dụ này, thuộc tính `target="_blank"` được sử dụng để chỉ định liên kết sẽ mở trong một tab mới.

<br>

**Thẻ danh sách không thứ tự (Unordered list):** Thẻ danh sách không thứ tự được sử dụng để tạo các danh sách không có thứ tự.

`ul` - Unordered list

`li` - List item

```html
  <ul>
    <li>Mục 1</li>
    <li>Mục 2</li>
    <li>Mục 3</li>
  </ul>
```
<br>

**Thẻ bảng (Table):** Thẻ bảng được sử dụng để tạo các bảng dữ liệu.

`table` - (table)
- `thead` - (table head)
  - `th` - (table heading)
- `tbody` - (table body)
  - `tr` - (table row)
    - `td` - (table data)

<br>

```html
  <table>
    <thead>
      <tr>
        <th>Tiêu đề cột 1</th>
        <th>Tiêu đề cột 2</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Dữ liệu cột 1</td>
        <td>Dữ liệu cột 2</td>
      </tr>
      <tr>
        <td>Dữ liệu cột 1</td>
        <td>Dữ liệu cột 2</td>
      </tr>
    </tbody>
  </table>
```
<br>

**Thẻ thẻ nhập liệu (Input):** Thẻ thẻ nhập liệu được sử dụng để tạo các trường nhập liệu cho người dùng.

`input`
- `type`: text
- `type`: checkbox
- `type`: radio

<br>

```html
  <input type="text" placeholder="Nhập tên">
  <input type="checkbox" name="gender" value="male">
  <input type="radio" name="gender" value="female">
  <button type="submit">Gửi</button>
```
<br>

**Thẻ phân chia (Division):** Thẻ phân chia được sử dụng để phân chia nội dung trang web thành các phần.

```html
  <div>Phần 1</div>
  <div>Phần 2</div>
```
