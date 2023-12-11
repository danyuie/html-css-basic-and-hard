# **RESPONSIVE & ADAPTIVE**

## **1. RESPONSIVE**

**Ý nghĩa:** Responsive design là một phương pháp thiết kế mà chú trọng vào việc tạo ra trang web hoặc ứng dụng có khả năng phản ứng linh hoạt đối với kích thước màn hình khác nhau bằng cách sử dụng các kỹ thuật linh hoạt như Media Queries và Fluid Grids.

**Điểm mạnh:**

* **Phản ứng linh hoạt:** Dự án có thể hiển thị đúng trên nhiều loại thiết bị và kích thước màn hình.
* **Duy trì một mã nguồn:** Chỉ cần duy trì một mã nguồn chung cho tất cả các thiết bị.

**Điểm yếu:**

* **Hiệu suất:** Có thể đôi khi gặp vấn đề hiệu suất trên các thiết bị có cấu hình thấp.
* **Phức tạp hóa thiết kế:** Một số trang web lớn có thể trở nên phức tạp khi phải xử lý nhiều điều kiện đáp ứng.



## **2. ADAPTIVE**

**Ý nghĩa:** Adaptive design tập trung vào việc tạo ra các phiên bản riêng biệt của trang web hoặc ứng dụng cho từng loại thiết bị hoặc kích thước màn hình cụ thể.

**Điểm mạnh:**

* **Kiểm soát chặt chẽ:** Có thể kiểm soát chặt chẽ hơn đối với trải nghiệm người dùng trên từng loại thiết bị.
* **Hiệu suất tốt:** Phiên bản dành cho từng thiết bị có thể được tối ưu hóa hiệu suất.

**Điểm yếu:**
* **Nhiều mã nguồn:** Cần duy trì nhiều phiên bản mã nguồn cho từng loại thiết bị, điều này có thể tăng công đồng và chi phí phát triển.
* **Khả năng hạn chế:** Khó khăn khi phải đối mặt với các thiết bị mới mà bạn chưa tích hợp sẵn trong chiến lược adaptive.

## **3. CÁCH VIẾT Ở CSS**

Trong ví dụ này, chúng ta sử dụng media queries để xác định các điều kiện môi trường khác nhau và điều chỉnh các thuộc tính của `.container` để làm cho nó phản ứng với kích thước màn hình.

```css
/* CSS chung cho tất cả các thiết bị */
.container {
  width: 100%;
  margin: 0 auto;
  box-sizing: border-box;
}

/* Responsive styles cho màn hình nhỏ (mobile) */
@media only screen and (max-width: 767px) {
  .container {
    padding: 10px;
  }
}

/* Responsive styles cho tablet */
@media only screen and (min-width: 768px) and (max-width: 1023px) {
  .container {
    padding: 20px;
  }
}

/* Responsive styles cho desktop và các màn hình lớn hơn */
@media only screen and (min-width: 1024px) {
  .container {
    padding: 30px;
  }
}

```

## **3. CÁCH VIẾT Ở SCSS**

Dưới đây là một ví dụ về một mixin Sass đơn giản để sử dụng trong responsive design. Mixin này sử dụng Sass's `@media` để xác định các điều kiện môi trường khác nhau.

```scss
// Mixin cho responsive design
@mixin responsive($breakpoint) {
  @if $breakpoint == mobile {
    @media only screen and (max-width: 767px) {
      @content;
    }
  }

  @if $breakpoint == tablet {
    @media only screen and (min-width: 768px) and (max-width: 1023px) {
      @content;
    }
  }

  @if $breakpoint == desktop {
    @media only screen and (min-width: 1024px) {
      @content;
    }
  }
}

// Sử dụng mixin
.example {
  width: 100%;

  @include responsive(mobile) {
    width: 50%;
  }

  @include responsive(tablet) {
    width: 75%;
  }

  @include responsive(desktop) {
    width: 100%;
  }
}
```

Trong đoạn mã trên, `@mixin responsive` là mixin chúng ta đã tạo. Nó cho phép bạn định nghĩa các quy tắc CSS cụ thể cho từng loại breakpoint (mobile, tablet, desktop). Khi bạn sử dụng mixin này trong một rule CSS, nó sẽ được biên dịch thành các luật tương ứng trong các điều kiện môi trường khác nhau.

Áp dụng trong sass:

```scss
// Mixin cho responsive design
@mixin responsive($breakpoint)
  @if $breakpoint == mobile
    @media only screen and (max-width: 767px)
      @content
  @if $breakpoint == tablet
    @media only screen and (min-width: 768px) and (max-width: 1023px)
      @content
  @if $breakpoint == desktop
    @media only screen and (min-width: 1024px)
      @content

// Sử dụng mixin
.example
  width: 100%

  +responsive(mobile)
    width: 50%

  +responsive(tablet)
    width: 75%

  +responsive(desktop)
    width: 100%
```

Chú ý rằng trong Sass, chúng ta sử dụng dấu cộng `+` để gọi mixin thay vì `@include`. Ngoài ra, bạn không cần dấu ngoặc nhọn cho các điều kiện `@if` trong Sass.

## **4. CÁC BREAKPOINT**

**responsive:**
* sm: 320px
* md: 768px
* lg: 1024px

**Adaptive:**
* 320px
* 480px
* 768px
* 1024px
* xl: 1200px
* 1xl: 1366px
* 2xl: 1440px
* 3xl: 1600px
* 4xl: 1920px