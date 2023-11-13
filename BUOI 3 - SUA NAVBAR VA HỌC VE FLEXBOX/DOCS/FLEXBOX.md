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

**Thành phần quan trọng nhất của Flexbox là:**

- **container:** là thành phần lớn bao quanh các phần tử bên trong, các item bên trong sẽ hiển thị dựa trên thiết lập của container này.
- **item:** là phần tử con của container, bạn có thể thiết lập nó sẽ sử dụng bao nhiêu cột trong một container, hoặc thiết lập thứ tự hiển thị của nó.

| Container      | Items |
| ----------- | ----------- |
|![](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-2.jpg)|![](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-3.jpg)|

### **3. Các thuộc tính của Flex Container**

<br>

<p align="center">
  <img width="80%" height="80%" src="https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-4.jpg">
</p>

**Display**

Để sử dụng flex trong css thì đơn giản là chúng ta chỉ cần khai báo thuộc tính `display: flex`

```css
.container { 

  display: flex; /* hoặc inline-flex */ 

  }
```

> [!NOTE]
> Lưu ý: các cột CSS thông thường không sử dụng được trong flex container.

**Flex-direction**

Thuộc tính **flex-direction** xác định hướng của **main-axis** để container sắp xếp các item.

<p align="center">

|||
| --------------------------------------- | ------------------------------------- |
|![img](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-5.jpg)|![img](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-6.jpg)|
</p>

**Cú pháp**

```css
.container {    

  flex-direction: row | row-reverse | column | column-reverse;  

  }
```

**Các tham số:**

- **row:** mặc định, flex item được sắp xếp theo chiều ngang, từ trái qua phải (main axis nằm ngang).
- **row-reverse:** flex item được sắp xếp theo chiều ngang, từ phải qua trái (main axis nằm ngang).
- **column:** flex item được sắp xếp theo chiều dọc, từ trên xuống dưới (main axis đứng dọc).
- **column-reverse:** flex item được sắp xếp theo chiều dọc, từ dưới lên trên (main axis đứng dọc).

**Flex-wrap**

<img width="100%" height="100%" src="https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-7.jpg">

<br>

Theo mặc định, item sẽ tự động thay đổi kích thước phần tử để nó luôn hiển thị trên cùng một dòng dù bạn có resize trình duyệt theo kích thước nào, điều này dễ làm cho nội dung bên trong (nếu có) bị giãn hay ép nhỏ lại, có thể gây xấu giao diện.

Vì vậy, ta có **thuộc tính flex-wrap** cho phép item tự động xuống dòng khi kích thước container thay đổi.

**Cú pháp**

```css
.container{

  flex-wrap: nowrap | wrap | wrap-reverse; 

  }
```

**Tham số:**

- **nowrap:** mặc định, tất cả các item sẽ nằm trên một dòng.
- **wrap:** khi kích thước container thay đổi và tổng chiều rộng các item cộng lại lớn hơn chiều rộng của container thì item sẽ tự động xuống dòng.
- **wrap-reverse:** tương tự như wrap, nhưng thay vì xuống dòng thì item sẽ tự động nhảy lên trên.

**Justify-content**

<p align="center">

|||
|---|---|
|![](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-13.jpg)|![](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-16.jpg)|
|![](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-17.jpg)|![](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-18.jpg)|
|![](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-19.jpg)|![](https://topdev.vn/blog/wp-content/uploads/2020/10/flexbox-20.jpg)|

</p>

Theo mặc định, các item bên trong sẽ bắt đầu từ main start đến main end, tuy nhiên, đôi khi container vẫn còn khoảng trống. Vì vậy, bạn có thể sử dụng **thuộc tính justify-content** để điều chỉnh vị trí bắt đầu và căn chỉnh các item bên trong container theo **dọc theo trục main axis**, chiều ngang hoặc chiều dọc tùy thuộc vào flex-direction.

**Cú pháp**

```css
.container{

  justify-content: flex-start | flex-end | center |
                    space-between | space-around | space-evenly;

  }
```

**Các tham số:**

- **flex-start:** giá trị mặc định, item sẽ bắt đầu từ lề chính main-start của container.
- **flex-end:** item sẽ bắt đầu từ lề chính main-end của container (khác với row-reverse là đổi hướng hiển thị).
- **center:** item sẽ nằm giữa container.
- **space-between:** các item sẽ có khoảng cách giữa các phần tử bằng nhau do container sẽ tự động căn khoảng cách, item đầu tiên sát lề chứa điểm main-start, item cuối cùng sát lề chứa điểm main-end.
- **space-around:** tương tự space-between, nhưng khác ở chỗ là mỗi item có khoảng cách 2 bên cạnh và những khoảng cách này bằng nhau.
- **space-evenly:** các item được phân phối sao cho khoảng cách giữa hai item bất kỳ, giữa item và các lề là bằng nhau.

**Align-items**

**Thuộc tính align-items** sử dụng để điều chỉnh vị trí bắt đầu và căn chỉnh các item bên trong container theo dọc theo trục cross axis, chiều ngang hoặc chiều dọc tùy thuộc vào flex-direction.

**Cú pháp**

```css
.container{

  align-items: stretch | flex-start | flex-end | center | baseline;

  }
```

