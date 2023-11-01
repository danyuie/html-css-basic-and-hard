# SETUP PHẦN MỀM VÀ CÁC EXTENSIONS 

</br>

### **1. Cài đặt Studio Visual Code**

Cài đặt **Studio Visual Code** ở link này [Bấm Vào Đây](https://code.visualstudio.com/download)




### **2. Cài đặt Font Chữ Mono SF**

Cài đặt **Font SF Mono** ở link này [Bấm Vào Đây](https://github.com/supercomputra/SF-Mono-Font)


### **3. Cài đặt Extension**

Các **Extension** cần thiết để hỗ trợ code.
| Tên | Tác Dụng |
| -------- | ------- |
| **Auto Close Tag** | Tự động đóng tag |
| **Color Hightlight** | Hiển thị màu khi code css |
| **Live Server** | Tự động re-fresh trình duyện khi lưu file |
| **Material Icon Theme** | Icon File |
| **Atom One Dark Theme** | Theme của trình code giúp đễ nhận diện tag và chống đau mắt |
| **GitLens - Git supercharged** | Ghi chú chỉnh sửa code trên worktree |
| **Auto Close Tag** | Tự động đóng tag |



### **4. Cài đặt và sử đụng Git để lưu trữ dự án**

Cài đặt **Git** ở link này [Bấm Vào Đây](https://git-scm.com/)
. Ở lần đầu tiên cài đặt, mở terminal và khai báo tác giả cho hệ thống Git ghi nhận.

**1. Set username** 
```
git config --global user.name "FIRST_NAME LAST_NAME"
```
**2. Set gmail** 
```
git config --global user.email "MY_NAME@example.com"
```
**3. Một số lệnh cơ bản trong Git**

- Dùng để tạo kho lưu trữ ở local
  ```
  git init 
  ```
- Tạo 1 nhánh mới có tên là main
  ```
  git branch -M main
  ```
- Thêm các file mới vào kho lưu trữ
  ```
  git add . 
  ```
- Thêm các ghi chú sau khi thêm file xong. bắt buộc 
  ```
  git commit -m "your commit" 
  ```
- Set đường link kho lưu trữ online ở github.com
  ```
  git remote add origin URl
  ```
- đẩy file từ kho lưu trữ local lên nhánh main trên kho online
  ```
  git push origin main
  ```