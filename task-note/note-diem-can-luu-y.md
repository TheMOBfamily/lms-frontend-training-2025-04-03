# **ĐIỂM QUAN TRỌNG CẦN LƯU Ý - FRONTEND**

## **CÁC VẤN ĐỀ RESPONSIVE PHỔ BIẾN**

-   Mobile menu không hiện đúng trên màn hình nhỏ
-   Overflow horizontal trên trang quiz
-   Font size quá nhỏ trên mobile
-   Button bị chồng lấp ở breakpoint 768px
-   Container width không thay đổi theo đúng breakpoints

## **THÀNH PHẦN CẦN ƯU TIÊN FIX**

1. **Homepage**: Hero section, featured courses
2. **Quiz Page**: Quiz container, câu hỏi và đáp án
3. **Video Player**: Controls và subtitle
4. **Checkout Pages**: Form fields và buttons
5. **User Dashboard**: Navigation và content display

## **CSS PERFORMANCE ISSUES**

-   Quá nhiều `!important` trong CSS
-   Selectors quá phức tạp (>4 levels)
-   Thiếu modular organization
-   Nhiều styles trùng lặp giữa theme và plugin

## **ASSETS MANAGEMENT**

-   Chưa tối ưu hóa images
-   JS không được minify
-   Chưa có lazy loading cho images và components
-   Font loading không hiệu quả

## **BROWSER SUPPORT**

-   Cần support cho:
    -   Chrome (>90)
    -   Firefox (>85)
    -   Safari (>14)
    -   Edge (>90)
    -   Mobile browsers

## **GIT WORKFLOW**

-   Branch chính: `main`
-   Branch của team dev: `dev1`, `dev2`, v.v.
-   Quy trình làm việc:
    1. Luôn tách branch riêng cho mỗi công việc
    2. Đặt tên branch: `fix/[issue-name]` hoặc `feature/[feature-name]`
    3. Sau khi hoàn thành, tạo Pull Request vào branch dev tương ứng
    4. KHÔNG tạo Pull Request trực tiếp vào `main`
-   Commit message format: `[scope]: [short description]`
