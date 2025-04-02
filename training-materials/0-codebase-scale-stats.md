# Thống Kê Các Dự Án PHP và Plugin WordPress

> Cập nhật: 2025-04-03

## 1. Các Dự Án PHP Lớn

| **Dự Án**   | **Số lượng Tệp** | **Dòng Mã (LOC)** |
| ----------- | ---------------- | ----------------- |
| Drupal      | ~17.000          | ~1.300.000        |
| Symfony     | ~8.000           | ~900.000          |
| WordPress   | ~3.000           | ~600.000          |
| CodeIgniter | ~1.500           | ~150.000          |
| Laravel     | ~400             | ~15.000           |

## 2. Plugin WordPress Phổ Biến

| **Plugin**           | **Số lượng Tệp** | **Dòng Mã (LOC)** |
| -------------------- | ---------------- | ----------------- |
| Elementor            | 1.803            | 593.414           |
| WooCommerce          | 4.321            | 404.805           |
| Deutschfuns Codebase | 3.991            | 304.921           |
| UpdraftPlus          | 1.192            | 222.937           |
| Yoast SEO            | 1.375            | 79.036            |

## 3. Dự Án Deutschfuns

| **Dự Án**               | **Số lượng Tệp** | **Dòng Mã (LOC)** | **Tổng LOC** |
| ----------------------- | ---------------- | ----------------- | ------------ |
| Fong De LMS Plugin      | 3.748            | 285.050           | 304.921      |
| Astra Child Deutschfuns | 243              | 19.871            |              |

## Ghi Chú

1. Số liệu được cập nhật vào tháng 4/2025
2. LOC (Lines of Code) bao gồm cả code, comment và dòng trống

## So Sánh Quy Mô

### 1. So sánh Deutschfuns với WordPress Core

```
WordPress Core vs Deutschfuns (LOC)
600K ┌────────────────────────────────────────┐
     │████████████████████████████████████████│ WordPress (600.000)
     │                                        │
300K │██████████████████████                  │ Deutschfuns (304.921)
     └────────────────────────────────────────┘
```

```
WordPress Core vs Deutschfuns (Files)
4000 ┌────────────────────────────────────────┐
     │████████████████████████████████████████│ Deutschfuns (3.991)
     │                                        │
3000 │██████████████████████████████          │ WordPress (3.000)
     └────────────────────────────────────────┘
```

### 2. So sánh Deutschfuns với các Plugin Phổ biến

```
LOC So sánh (K = 1000 LOC)
600K ┌────────────────────────────────────────┐
     │████████████████████████████████████    │ Elementor (593K)
     │████████████████████████                │ WooCommerce (404K)
     │███████████████████                     │ Deutschfuns (304K)
     │████████████                            │ UpdraftPlus (222K)
     │████                                    │ Yoast SEO (79K)
     └────────────────────────────────────────┘
```

```
Files So sánh
5000 ┌────────────────────────────────────────┐
     │████████████████████████████████████    │ WooCommerce (4.321)
     │██████████████████████████████          │ Deutschfuns (3.991)
     │███████████████                         │ Elementor (1.803)
     │██████████                              │ Yoast SEO (1.375)
     │████████                                │ UpdraftPlus (1.192)
     └────────────────────────────────────────┘
```

### 3. Phân Tích So Sánh

1. **So với WordPress Core:**

    - Deutschfuns có khoảng 50.8% số LOC của WordPress Core
    - Deutschfuns có nhiều tệp hơn WordPress Core (133%)

2. **So với các Plugin khác:**
    - LOC: Đứng thứ 3 sau Elementor và WooCommerce
    - Số lượng tệp: Đứng thứ 2 sau WooCommerce
    - Quy mô tương đối lớn cho một plugin tự phát triển
