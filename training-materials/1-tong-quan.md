# **1. TỔNG QUAN HỆ THỐNG DEUTSCHFUNS**

## **🌐 Giới thiệu**

**Deutschfuns.com** là nền tảng học tiếng Đức trực tuyến với mục tiêu cung cấp các khóa học tiếng Đức từ cơ bản đến nâng cao, kèm theo các công cụ học tập hiệu quả như bài tập tương tác, từ điển, video bài giảng, và thi thử.

## **⚙️ Công nghệ sử dụng**

### **Core Technologies**

-   **WordPress 6.7.2**: Nền tảng CMS chính
-   **PHP 8.x**: Ngôn ngữ lập trình backend
-   **MySQL/MariaDB**: Cơ sở dữ liệu
-   **JavaScript/jQuery**: Frontend interactivity
-   **HTML5/CSS3**: Markup và styling

### **Themes**

-   **Astra Theme**: Theme chính (parent)
-   **Astra Child Theme (deutschfuns)**: Theme con tùy chỉnh

### **Plugin chính**

1. **LearnDash LMS**: Hệ thống quản lý học tập
2. **Advanced Custom Fields (ACF)**: Quản lý trường tùy chỉnh
3. **Redux Framework**: Framework quản lý tùy chọn theme
4. **PODs**: Quản lý custom post types và fields
5. **Fong_De_LMS**: Plugin tùy chỉnh chính của dự án

## **📂 Cấu trúc dự án**

### **Cấu trúc thư mục chính**

```
/wp-content/
├── themes/
│   ├── astra/                  # Parent theme
│   └── astra-child-deutschfuns/  # Child theme (customizations)
│       ├── style.css           # Main stylesheet
│       ├── functions.php       # Theme functions
│       └── assets/             # CSS, JS, images
│
└── plugins/
    └── fong_de_lms/            # Main custom plugin
        ├── fong_de_lms.php     # Plugin entry file
        ├── includes/           # Core functionality
        ├── modules/            # Feature modules (30+)
        │   ├── module-1/       # Each module is self-contained
        │   │   ├── src/public/css/  # Module CSS
        │   │   ├── src/public/js/   # Module JS
        │   │   └── templates/  # Module templates
        │   └── module-2/
        │       └── ...
        ├── _figma/             # Figma design references
        ├── public/             # Public assets
        │   ├── js/             # 80+ JavaScript files
        │   ├── css/            # 15+ CSS files
        │   └── ...
        └── assets/             # Shared assets
```

## **🧩 Modules**

Plugin **Fong_De_LMS** chứa hơn 30 modules, mỗi module là một chức năng độc lập. Các module chính bao gồm:

1. **dquiz**: Module quản lý và hiển thị bài tập tương tác
2. **video**: Quản lý và phát video bài giảng
3. **tu-dien**: Từ điển tiếng Đức - tiếng Việt
4. **thi-thu**: Hệ thống thi thử và đánh giá
5. **users**: Quản lý người dùng và quyền truy cập
6. **learning-package**: Quản lý gói học và subscription
7. **và nhiều module khác...**

## **🎯 Mục tiêu đào tạo**

Sau khi hoàn thành chương trình đào tạo, frontend developer sẽ có khả năng:

1. **Hiểu rõ cấu trúc dự án** và vị trí các file CSS/JS
2. **Chỉnh sửa và tùy biến giao diện** theo yêu cầu
3. **Fix lỗi responsive** trên các thiết bị khác nhau
4. **Tối ưu hóa hiệu suất** frontend
5. **Tuân thủ các quy tắc code** và coding standards
6. **Phối hợp hiệu quả** với team backend

## **🚀 Các nhiệm vụ chính**

1. **Fix giao diện hiện tại** để responsive trên tất cả thiết bị
2. **Tối ưu hóa trải nghiệm người dùng** trên thiết bị di động
3. **Hỗ trợ phát triển** các tính năng và giao diện mới
4. **Bảo trì và cải thiện** code CSS/JS hiện có
5. **Triển khai thiết kế** từ Figma sang code

## **📚 Tài liệu tham khảo**

-   [WordPress Developer Resources](https://developer.wordpress.org/)
-   [Astra Theme Documentation](https://wpastra.com/docs/)
-   [LearnDash LMS Documentation](https://www.learndash.com/support/)
-   [BEM Methodology for CSS](https://en.bem.info/methodology/)
-   [ES6 JavaScript Features](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

~ from global rules
