# **2. CẤU TRÚC PLUGIN FONG_DE_LMS**

## **🔌 Giới thiệu Plugin**

Plugin **Fong_De_LMS** là plugin tùy chỉnh chính của hệ thống Deutschfuns, được phát triển để mở rộng chức năng của WordPress và LearnDash LMS. Plugin cung cấp nhiều tính năng đặc thù cho việc học tiếng Đức, từ bài tập tương tác đến từ điển trực tuyến.

## **📂 Thư mục gốc plugin**

```
F:\Dropbox\localwp\tiengduc2fongcom\app\public\wp-content\plugins\fong_de_lms\
```

## **📄 File chính**

-   **fong_de_lms.php**: Entry point của plugin, chứa thông tin plugin và khởi tạo các components
-   **.files-lms.md**: Tài liệu về cấu trúc file của plugin
-   **composer.json**: Quản lý dependencies PHP

## **🧩 Modules**

Plugin chứa hơn 30 modules khác nhau, mỗi module nằm trong thư mục `/modules/`. Dưới đây là một số module chính:

### **Module dquiz**

-   **Mục đích**: Quản lý và hiển thị bài tập tương tác
-   **Vị trí**: `/modules/dquiz/`
-   **CSS/JS**: `/modules/dquiz/dquiz3/src/public/css/` và `/modules/dquiz/dquiz3/src/public/js/`

### **Module video**

-   **Mục đích**: Quản lý và phát video bài giảng
-   **Vị trí**: `/modules/video/`
-   **CSS/JS**: `/modules/video/src/public/css/` và `/modules/video/src/public/js/`

### **Module tu-dien**

-   **Mục đích**: Từ điển tiếng Đức - tiếng Việt
-   **Vị trí**: `/modules/tu-dien/`
-   **CSS/JS**: `/modules/tu-dien/src/public/css/` và `/modules/tu-dien/src/public/js/`

### **Module thi-thu**

-   **Mục đích**: Hệ thống thi thử và đánh giá
-   **Vị trí**: `/modules/thi-thu/`
-   **CSS/JS**: `/modules/thi-thu/src/public/css/` và `/modules/thi-thu/src/public/js/`

### **Module users**

-   **Mục đích**: Quản lý người dùng và quyền truy cập
-   **Vị trí**: `/modules/users/`
-   **CSS/JS**: `/modules/users/src/public/css/` và `/modules/users/src/public/js/`

### **Cấu trúc chung của module**

```
/modules/[module-name]/
├── .files-[module-name].md  # Tài liệu module
├── init-[module-name].php   # File khởi tạo module
├── src/
│   ├── public/
│   │   ├── css/            # CSS files
│   │   ├── js/             # JavaScript files
│   │   └── images/         # Images
│   ├── templates/          # Template files
│   ├── controllers/        # Controller files
│   ├── helpers/            # Helper functions
│   └── services/           # Service classes
└── config/                 # Configuration
```

## **📁 Thư mục public**

Thư mục `/public/` chứa các file CSS và JS chung cho toàn bộ plugin, không thuộc về module cụ thể nào.

### **CSS files (`/public/css/`)**

-   **fong-style-frontend.css**: Stylesheet chính cho frontend
-   **fong-style-tu-dien-frontend.css**: Stylesheet cho từ điển
-   **fong-audio-player.css**: Stylesheet cho audio player
-   **fong-login.css**: Stylesheet cho login pages
-   **fong-popup-2.css**: Stylesheet cho popups
-   **fong-quiz-wrong-answer-popup.css**: Stylesheet cho quiz wrong answer popups
-   **+ 9 files CSS khác**

### **JS files (`/public/js/`)**

-   **fong-script-frontend.js**: JavaScript chính cho frontend
-   **fong-bai-tap-frontend.js**: JavaScript cho bài tập
-   **fong-script-tu-dien-frontend.js**: JavaScript cho từ điển
-   **fong-page-transitions.js**: JavaScript cho page transitions
-   **fong-login.js**: JavaScript cho login pages
-   **fong-load-quiz-results.js**: JavaScript cho quiz results
-   **+ 30 files JS khác**

### **Thư mục modules JS (`/public/js/modules/`)**

Chứa các JavaScript modules theo chuẩn ES6 được tổ chức theo chức năng.

### **Thư mục helpers JS (`/public/js/helpers/`)**

Chứa các helper functions JavaScript được sử dụng trong nhiều modules khác nhau.

## **👨‍💻 Quy tắc code JavaScript**

-   **ES6+ Standards**: Sử dụng chuẩn ES6 trở lên
-   **Module Pattern**: Ưu tiên sử dụng module pattern
-   **Named Exports**: Không sử dụng export default
-   **Prefix**: Sử dụng prefix `fong` cho các functions, classes, và biến toàn cục
-   **Constants**: SCREAMING_SNAKE_CASE cho constants
-   **Async/Await**: Ưu tiên sử dụng async/await thay vì callbacks
-   **Lỗi**: Sử dụng try/catch và Promise error handling

### **Ví dụ JavaScript**

```javascript
// ĐÚNG: Object Literal Pattern
export const FongSomeModule = {
    init() {
        // Initialization code
    },

    processData(data) {
        // Process data
    },
};

// SAI: Export default
export default class SomeModule {
    // Class implementation
}
```

## **🎨 Quy tắc code CSS**

-   **BEM Methodology**: Block Element Modifier
-   **Prefix**: Sử dụng prefix `fong-` cho các class
-   **Mobile First**: Thiết kế mobile first, sau đó mở rộng lên desktop
-   **Media Queries**: Sử dụng breakpoints chuẩn (576px, 768px, 992px, 1200px)
-   **Variables**: Sử dụng CSS variables cho màu sắc và spacing

### **Ví dụ CSS (BEM)**

```css
/* Block */
.fong-card {
    padding: 1rem;
}

/* Element */
.fong-card__title {
    font-size: 1.5rem;
}

/* Modifier */
.fong-card--featured {
    border: 2px solid var(--fong-primary-color);
}

/* State */
.fong-card--is-active {
    background-color: var(--fong-highlight-bg);
}
```

## **🔄 Quy trình làm việc với plugin**

1. **Xác định module** cần chỉnh sửa
2. **Tìm file CSS/JS** trong module đó hoặc trong thư mục `/public/`
3. **Tạo branch mới** trong Git
4. **Chỉnh sửa** và test trên local
5. **Commit và push** lên repository
6. **Tạo pull request** để review

## **⚠️ Lưu ý quan trọng**

-   **KHÔNG** chỉnh sửa trực tiếp các file JS trong `/public/js/` mà không hỏi ý kiến Mr. Toàn trước
-   Ưu tiên chỉnh sửa CSS trước khi chỉnh sửa JS
-   Tuân thủ các quy tắc đặt tên và coding standards
-   Kiểm tra tính tương thích trên nhiều trình duyệt và thiết bị
-   Sử dụng Developer Tools để debug trước khi commit

## **📚 Tài liệu tham khảo**

-   `.files-lms.md`: Tài liệu chi tiết về cấu trúc file plugin
-   `.files-[module-name].md`: Tài liệu chi tiết về module cụ thể
-   Các file trong thư mục `/docs/`

~ from global rules
