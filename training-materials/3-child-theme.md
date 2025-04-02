# **3. CẤU TRÚC ASTRA CHILD THEME**

## **🎨 Giới thiệu Child Theme**

**Astra Child Theme (deutschfuns)** là theme con tùy chỉnh được xây dựng trên Astra Parent Theme. Child theme cho phép tùy chỉnh giao diện và chức năng mà không ảnh hưởng đến parent theme, đảm bảo khả năng cập nhật an toàn.

## **📂 Thư mục gốc child theme**

```
F:\Dropbox\localwp\tiengduc2fongcom\app\public\wp-content\themes\astra-child-deutschfuns\
```

## **📄 File chính**

-   **style.css**: Stylesheet chính của child theme, chứa thông tin theme và CSS cơ bản
-   **functions.php**: File core của child theme, chứa hooks, functions, và enqueue scripts/styles
-   **header.php**: Template cho header
-   **footer.php**: Template cho footer
-   **single.php**: Template cho single post
-   **404.php**: Template cho error 404
-   **.files-astra-childtheme.md**: Tài liệu về cấu trúc file của child theme

## **📁 Thư mục assets**

Thư mục `/assets/` chứa các file CSS, JS, fonts và images của child theme.

### **CSS files (`/assets/css/`)**

-   **fong-register.css**: Stylesheet cho trang đăng ký
-   **fong-login.css**: Stylesheet cho trang đăng nhập
-   **fong-profile.css**: Stylesheet cho trang profile
-   **fong-tu-dien.css**: Stylesheet cho trang từ điển
-   **fong-tu-vung.css**: Stylesheet cho trang từ vựng
-   **fong-thi-thu-selector.css**: Stylesheet cho trang chọn bài thi thử
-   **fong-menu-footer-bar.css**: Stylesheet cho menu footer
-   **fong-khoa-hoc.css**: Stylesheet cho trang khóa học
-   **fong-home.css**: Stylesheet cho trang chủ
-   **fong-chi-tiet-khoa-hoc.css**: Stylesheet cho trang chi tiết khóa học
-   **+ 15 files CSS khác**

### **JS files (`/assets/js/`)**

-   **init-fong-register.js**: JavaScript cho trang đăng ký
-   **fong-login.js**: JavaScript cho trang đăng nhập
-   **fong-profile.js**: JavaScript cho trang profile
-   **fong-tu-dien.js**: JavaScript cho trang từ điển
-   **fong-tu-vung.js**: JavaScript cho trang từ vựng
-   **fong-menu-footer-bar.js**: JavaScript cho menu footer
-   **fong-khoa-hoc.js**: JavaScript cho trang khóa học
-   **fong-home.js**: JavaScript cho trang chủ
-   **fong-chi-tiet-khoa-hoc.js**: JavaScript cho trang chi tiết khóa học
-   **+ 10 files JS khác**

### **Thư mục `/assets/js/modules-learndash-sidebar/`**

Chứa các JavaScript modules cho sidebar của LearnDash.

### **Thư mục `/assets/js/register/`**

Chứa các JavaScript modules cho chức năng đăng ký.

## **📁 Thư mục templates**

Thư mục `/templates/` chứa các template files cho các trang tùy chỉnh.

## **📁 Thư mục template-parts**

Thư mục `/template-parts/` chứa các thành phần template có thể tái sử dụng.

## **📁 Thư mục learndash**

Thư mục `/learndash/` chứa các template override cho LearnDash.

## **📁 Thư mục woocommerce**

Thư mục `/woocommerce/` chứa các template override cho WooCommerce.

## **📁 Thư mục deutschfuns-controllers và deutschfuns-enqueue**

-   `/deutschfuns-controllers/`: Chứa các controller files
-   `/deutschfuns-enqueue/`: Chứa các file enqueue scripts và styles

## **🔄 Cách Theme Override Hoạt Động**

WordPress sẽ ưu tiên sử dụng template từ child theme trước khi sử dụng template từ parent theme. Quy trình như sau:

1. WordPress tìm kiếm template trong child theme
2. Nếu không tìm thấy, WordPress sẽ sử dụng template từ parent theme
3. CSS của child theme được load sau CSS của parent theme, cho phép override styles

## **👨‍💻 Quy trình làm việc với Child Theme**

1. **Xác định trang** cần chỉnh sửa (ví dụ: home, profile, khóa học...)
2. **Tìm file CSS/JS** tương ứng trong thư mục `/assets/css/` hoặc `/assets/js/`
3. **Chỉnh sửa CSS/JS** để đạt được giao diện mong muốn
4. **Test trên các thiết bị** khác nhau
5. **Commit và push** lên repository

## **🎨 Hướng dẫn CSS cho Child Theme**

### **1. Overriding Parent Theme Styles**

```css
/* Original style in parent theme */
.site-title {
    font-size: 26px;
}

/* Override in child theme's style.css */
.site-title {
    font-size: 32px;
    font-weight: bold;
    color: #007bff;
}
```

### **2. Sử dụng CSS Variables**

```css
:root {
    --fong-primary-color: #007bff;
    --fong-secondary-color: #6c757d;
    --fong-success-color: #28a745;
    --fong-font-family: "Montserrat", sans-serif;
}

.fong-button {
    background-color: var(--fong-primary-color);
    font-family: var(--fong-font-family);
}

.fong-button--secondary {
    background-color: var(--fong-secondary-color);
}
```

### **3. Responsive Design với Media Queries**

```css
/* Mobile first styles */
.fong-course-card {
    width: 100%;
    padding: 1rem;
}

/* Tablet styles */
@media (min-width: 768px) {
    .fong-course-card {
        width: 50%;
    }
}

/* Desktop styles */
@media (min-width: 992px) {
    .fong-course-card {
        width: 33.333%;
    }
}
```

## **🔄 Enqueue Scripts và Styles**

Child theme sử dụng các functions trong `functions.php` để enqueue CSS và JavaScript files. Ví dụ:

```php
// Enqueue parent theme's style.css first
wp_enqueue_style('astra-theme-css', get_template_directory_uri() . '/style.css');

// Then enqueue child theme's style.css
wp_enqueue_style('deutschfuns-child-style', get_stylesheet_uri());

// Enqueue custom script
wp_enqueue_script('fong-home', get_stylesheet_directory_uri() . '/assets/js/fong-home.js', array('jquery'), '1.0.0', true);
```

## **⚠️ Lưu ý quan trọng**

-   **KHÔNG** chỉnh sửa trực tiếp parent theme
-   **KHÔNG** hard-code chức năng hoặc styles mà có thể được cung cấp bởi plugins
-   **Luôn** sử dụng các prefix phù hợp (`fong-`) để tránh xung đột
-   **Kiểm tra** tính tương thích với các phiên bản WordPress và theme mới
-   **Sử dụng** các hooks của WordPress và Astra theme để tùy chỉnh
-   **Giữ** child theme nhẹ và tối ưu, tránh bloat

## **📚 Tài liệu tham khảo**

-   [WordPress Child Theme Documentation](https://developer.wordpress.org/themes/advanced-topics/child-themes/)
-   [Astra Theme Documentation](https://wpastra.com/docs/)
-   `.files-astra-childtheme.md`: Tài liệu chi tiết về cấu trúc file của child theme

~ from global rules
