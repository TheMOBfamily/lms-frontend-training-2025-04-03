# Hướng Dẫn Phát Triển Module

> Cập nhật: 2025-04-03

## Cấu Trúc Module Chuẩn

```plaintext
module-name/
├───config/          # Cấu hình module
├───docs/           # Tài liệu module
└───src/            # Mã nguồn
    ├───backend/    # Admin
    │   ├───css/
    │   └───js/
    ├───public/     # Frontend
    │   ├───css/
    │   ├───js/
    │   └───images/
    ├───controllers/
    ├───helpers/
    ├───models/
    ├───services/
    └───templates/
```

## Quy Tắc Đặt Tên

### 1. Files

-   **PHP Classes:** `Fong_ModuleName_ClassName-class.php`
-   **Helpers:** `fong_module_name_helper-helper.php`
-   **Controllers:** `fong-module-name-controller.php`
-   **CSS:** `fong-module-name.css`
-   **JS:** `fong-module-name.js`

### 2. Functions & Classes

-   **Functions:** `fong_module_name_function_name()`
-   **Classes:** `Fong_ModuleName_ClassName`
-   **Hooks:** `fong_module_name_hook_name`

## File Bắt Buộc

1. **Init File:** `init-module-name.php`

    ```php
    <?php
    // Module initialization
    if (!defined('ABSPATH')) {
        exit;
    }
    ```

2. **Config File:** `config/module-config.php`

    ```php
    <?php
    // Module configuration
    return [
        'version' => '1.0.0',
        'dependencies' => []
    ];
    ```

3. **Documentation:** `docs/README.md`

    ```markdown
    # Module Name

    Version: 1.0.0
    Dependencies: [...]
    ```

## Quy Tắc Phát Triển

### 1. Initialization

```php
add_action('init', 'fong_module_name_init');
function fong_module_name_init() {
    // Module initialization code
}
```

### 2. Asset Loading

```php
add_action('wp_enqueue_scripts', 'fong_module_name_enqueue');
function fong_module_name_enqueue() {
    // Enqueue assets
}
```

### 3. AJAX Handlers

```php
add_action('wp_ajax_fong_module_action', 'fong_module_ajax_handler');
function fong_module_ajax_handler() {
    // Handle AJAX request
}
```

## Tích Hợp Module

1. **Autoloading**

    ```php
    require_once FONG_PLUGIN_PATH . 'modules/module-name/init-module-name.php';
    ```

2. **Dependencies**

    ```php
    add_action('plugins_loaded', 'fong_module_name_check_dependencies');
    ```

3. **Activation/Deactivation**
    ```php
    register_activation_hook(__FILE__, 'fong_module_name_activate');
    register_deactivation_hook(__FILE__, 'fong_module_name_deactivate');
    ```

## Testing & Debug

1. **Unit Tests**

    ```php
    class Fong_Module_Test extends WP_UnitTestCase {
        // Test cases
    }
    ```

2. **Debug Mode**
    ```php
    if (FONG_DEBUG) {
        // Debug code
    }
    ```

## Best Practices

1. **Modular Design**

    - Mỗi module hoạt động độc lập
    - Sử dụng dependency injection
    - Tránh hard dependencies

2. **Security**

    - Validate input data
    - Sanitize output
    - Check permissions

3. **Performance**

    - Cache kết quả
    - Optimize queries
    - Minimize asset loading

4. **Documentation**
    - PHPDoc cho functions/classes
    - README cho module
    - Changelog
