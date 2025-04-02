# Tài Liệu Tham Khảo File Quan Trọng

> Cập nhật: 2025-04-03

## Core Files

### Main Plugin File

```
/wp-content/plugins/fong_de_lms/fong_de_lms.php
```

### Constants & Config

```
/includes/constants/
├── fong-environment.php
├── fong-lms-main-constants.php
└── fong-message-constants.php
```

### Core Classes

```
/includes/classes/
├── FongPerformanceTracker-class.php
├── Fong_JWT_Handler-class.php
├── Fong_Performance_Optimizer-class.php
└── Fong_User_Metadata_Library-class.php
```

## Frontend Assets

### CSS Files

```
/public/css/
├── fong-de-lms-public.css      # Main frontend styles
├── fong-login.css              # Login page styles
├── fong-popup-2.css            # Popup component styles
└── montserrat-font.css         # Font definitions
```

### JavaScript Files

```
/public/js/
├── fong-de-lms-public.js       # Main frontend script
├── helpers/                    # JS helper functions
│   ├── FongDebug-class-helper.js
│   └── JsImporter-class-autoload.js
└── modules/                    # JS modules
    ├── fong-video-player-module.js
    └── fong-quiz-module.js
```

## Module Files

### Quiz Module

```
/modules/dquiz/
├── init-dquiz.php
└── src/
    ├── public/
    │   ├── css/
    │   └── js/
    └── templates/
```

### Video Module

```
/modules/video/
├── init-video.php
└── src/
    ├── public/
    │   ├── css/
    │   └── js/
    └── templates/
```

### User Module

```
/modules/users/
├── init-fong-role-user.php
└── src/
    ├── controllers/
    │   └── fong-user-management.php
    └── templates/
```

## Template Files

### Frontend Templates

```
/templates/
├── template-registration-page.php
├── template-update-profile.php
└── template-user-profile.php
```

### Admin Templates

```
/admin/templates/
├── template-admin-dashboard.php
└── template-user-management.php
```

## Debug & Development

### Debug Files

```
/fong-debug/
├── fong-debug.php
├── fong-dom-inspector.php
└── fong-performance-tracker.php
```

### Unit Tests

```
/fong-unit-tests/
├── _unit-test-FongDebug.php
└── _unit-test-import-module-es6-handler.php
```

## Documentation

### Module Documentation

```
/modules/[module-name]/docs/
├── README.md
└── CHANGELOG.md
```

### Project Documentation

```
/docs/
├── frontend-training-2025-04-03/
└── project-description/
```


> Cập nhật: 2025-04-03

## Core Files

### Main Plugin File

```
/wp-content/plugins/fong_de_lms/fong_de_lms.php
```

### Constants & Config

```
/includes/constants/
├── fong-environment.php
├── fong-lms-main-constants.php
└── fong-message-constants.php
```

### Core Classes

```
/includes/classes/
├── FongPerformanceTracker-class.php
├── Fong_JWT_Handler-class.php
├── Fong_Performance_Optimizer-class.php
└── Fong_User_Metadata_Library-class.php
```

## Frontend Assets

### CSS Files

```
/public/css/
├── fong-de-lms-public.css      # Main frontend styles
├── fong-login.css              # Login page styles
├── fong-popup-2.css            # Popup component styles
└── montserrat-font.css         # Font definitions
```

### JavaScript Files

```
/public/js/
├── fong-de-lms-public.js       # Main frontend script
├── helpers/                    # JS helper functions
│   ├── FongDebug-class-helper.js
│   └── JsImporter-class-autoload.js
└── modules/                    # JS modules
    ├── fong-video-player-module.js
    └── fong-quiz-module.js
```

## Module Files

### Quiz Module

```
/modules/dquiz/
├── init-dquiz.php
└── src/
    ├── public/
    │   ├── css/
    │   └── js/
    └── templates/
```

### Video Module

```
/modules/video/
├── init-video.php
└── src/
    ├── public/
    │   ├── css/
    │   └── js/
    └── templates/
```

### User Module

```
/modules/users/
├── init-fong-role-user.php
└── src/
    ├── controllers/
    │   └── fong-user-management.php
    └── templates/
```

## Template Files

### Frontend Templates

```
/templates/
├── template-registration-page.php
├── template-update-profile.php
└── template-user-profile.php
```

### Admin Templates

```
/admin/templates/
├── template-admin-dashboard.php
└── template-user-management.php
```

## Debug & Development

### Debug Files

```
/fong-debug/
├── fong-debug.php
├── fong-dom-inspector.php
└── fong-performance-tracker.php
```

### Unit Tests

```
/fong-unit-tests/
├── _unit-test-FongDebug.php
└── _unit-test-import-module-es6-handler.php
```

## Documentation

### Module Documentation

```
/modules/[module-name]/docs/
├── README.md
└── CHANGELOG.md
```

### Project Documentation

```
/docs/
├── frontend-training-2025-04-03/
└── project-description/
```
