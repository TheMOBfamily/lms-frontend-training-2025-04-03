# **ĐƯỜNG DẪN QUAN TRỌNG - DEUTSCHFUNS**

> Cập nhật: 2025-04-03

## Thống Kê Tổng Quan

-   Tổng số thư mục: 916
-   Tổng số file: 1370
-   Không bao gồm thư mục vendor

## Cấu Trúc Chính

```plaintext
deutschfuns/
├───wp-content/
│   ├───themes/
│   │   └───astra-child-deutschfuns/    # Child Theme
│   └───plugins/
│       └───fong_de_lms/                # Plugin Chính
│           ├───admin/                   # Quản trị backend
│           ├───includes/                # Core functionality
│           ├───modules/                 # Các module chức năng
│           ├───public/                  # Frontend assets
│           └───templates/               # Template files
```

## **PATHS CHÍNH**

### **1. Child Theme**

```
/wp-content/themes/astra-child-deutschfuns/
```

-   **CSS:** `/assets/css/`
-   **JS:** `/assets/js/`
-   **Images:** `/assets/images/`
-   **Templates:** `/template-parts/`

### **2. Plugin Core**

```
/wp-content/plugins/fong_de_lms/
```

#### 2.1. Core Files (`includes/`)

-   **Classes:** `/includes/classes/` - Các class cốt lõi
-   **Controllers:** `/includes/controllers/` - Xử lý logic chính
-   **Helpers:** `/includes/helpers/` - Các hàm tiện ích
-   **Constants:** `/includes/constants/` - Các hằng số và config

#### 2.2. Public Assets (`public/`)

-   **CSS:** `/public/css/` - Stylesheet files
-   **JS:** `/public/js/` - JavaScript files
-   **Images:** `/public/images/` - Media files

#### 2.3. Templates

-   **Templates:** `/templates/` - Template files chung

### **3. Modules**

```
/wp-content/plugins/fong_de_lms/modules/[module-name]/
```

Mỗi module có cấu trúc:

```plaintext
module-name/
├───config/          # Module config
├───docs/           # Module documentation
└───src/            # Source code
    ├───backend/    # Admin functionality
    │   ├───css/    # Admin styles
    │   └───js/     # Admin scripts
    ├───public/     # Frontend assets
    │   ├───css/    # Frontend styles
    │   ├───js/     # Frontend scripts
    │   └───images/ # Module images
    ├───controllers/# Logic handlers
    ├───helpers/    # Helper functions
    ├───models/     # Data models
    ├───services/   # Business logic
    └───templates/  # Module templates
```

## **MODULES QUAN TRỌNG**

1. **Quiz System** (`modules/dquiz/`)
2. **Video Player** (`modules/video/`)
3. **User Management** (`modules/users/`)
4. **Course System** (`modules/learndash/`)
5. **Dictionary** (`modules/tu-dien/`)
6. **Testing System** (`modules/thi-thu/`)
7. **Membership** (`modules/membership/`)
8. **Email System** (`modules/email/`)
9. **Private Message** (`modules/private-message/`)

## Quy Tắc Tổ Chức

1. **Modular:** Mỗi chức năng lớn được tách thành module riêng
2. **Separation of Concerns:** Tách biệt frontend/backend/logic
3. **Self-contained:** Mỗi module hoạt động độc lập
4. **Documentation:** Mỗi module có tài liệu riêng
