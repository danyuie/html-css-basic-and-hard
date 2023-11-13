# **CÁC THẺ CƠ BẢN TRONG HTML VÀ CSS**

### **1. Flexbox là gì**

**Flexbox** Layout (hay còn gọi là **Flexible Box**) là một kiểu bố cục trang có khả năng tự cân đối kích thước, thay đổi chiều rộng/chiều cao và thứ tự phần tử bên trong để phù hợp với tất cả các loại thiết bị hiển thị và kích thước màn hình.

Với bố cục thông thường, bạn cần phải thiết lập kích thước của phần tử, thiết lập hiển thị dạng block hay inline, cho nó float, còn với Flexbox bạn chỉ cần thiết lập phần hiển thị theo chiều ngang hay chiều dọc, lúc đó các phần tử bên trong có thể hiển thị theo ý muốn..

> [!NOTE]
> Lưu ý: Flexbox Layout phù hợp nhất để thiết lập bố cục ở quy mô nhỏ, còn thiết lập bố cục với phạm vi lớn hơn thì vẫn nên sử dụng kiểu thông thường là dàn trang theo dạng lưới (grid layout).

### **2 .Các khái niệm cơ bản và thuật ngữ**

**Bố cục Flex** được thiết lập từ một khung lớn (parent container) đóng vai trò là khung linh hoạt (flex containter) và các thẻ con ngay trong nó (immediate children) đóng vai trò các mục nhỏ linh hoạt (flex item).

![Alt text](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-1.jpg)
*Sơ đồ cấu trúc Flexbox.*

#### Thành phần quan trọng nhất của Flexbox là:

- **container:** là thành phần lớn bao quanh các phần tử bên trong, các item bên trong sẽ hiển thị dựa trên thiết lập của container này.
- **item:** là phần tử con của container, bạn có thể thiết lập nó sẽ sử dụng bao nhiêu cột trong một container, hoặc thiết lập thứ tự hiển thị của nó.

| Container      | Items |
| ----------- | ----------- |
|![](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-2.jpg)|![](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-3.jpg)|
