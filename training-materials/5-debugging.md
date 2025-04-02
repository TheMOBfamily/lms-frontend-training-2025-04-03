# **5. KỸ THUẬT DEBUG VÀ TROUBLESHOOTING**

## **🔍 CÔNG CỤ CHÍNH: CHROME DEVTOOLS**

Chrome DevTools là công cụ quan trọng nhất cho frontend developer:

-   **Elements Panel** (Ctrl+Shift+C): Kiểm tra HTML và CSS

    -   Xem/sửa DOM và CSS trực tiếp
    -   Kiểm tra Box Model (margin, padding, border)
    -   Xem Computed Styles để hiểu CSS đã áp dụng

-   **Console Panel** (Ctrl+Shift+J): Debug JavaScript

    -   `console.log()`/`console.error()` - hiển thị thông tin
    -   `console.table()` - hiển thị dữ liệu dạng bảng
    -   Xem JavaScript errors

-   **Network Panel** (Ctrl+Shift+E): Kiểm tra requests
    -   Xem API responses
    -   Kiểm tra thời gian tải
    -   Mô phỏng mạng chậm (Throttling)

## **🔄 QUY TRÌNH DEBUG**

1. **Tái hiện lỗi**: Xác định chính xác steps để tạo lỗi
2. **Kiểm tra Console**: Đọc thông báo lỗi JavaScript
3. **Xem Elements**: Kiểm tra HTML/CSS có vấn đề
4. **Kiểm tra Network**: Xem API có lỗi không
5. **Sửa lỗi**: Áp dụng giải pháp và test kỹ

## **🎯 DEBUG CSS PHỔ BIẾN**

-   **Thêm outline để debug layout**:

    ```css
    * {
        outline: 1px solid red;
    }
    ```

-   **Kiểm tra CSS không hoạt động**:

    1. Elements panel > chọn element
    2. Kiểm tra Styles panel
    3. Tìm CSS bị ghi đè (crossed out)

-   **Responsive bug**:
    1. Mở Device Mode (Ctrl+Shift+M)
    2. Test ở nhiều màn hình
    3. Tìm elements gây overflow

## **💻 DEBUG JAVASCRIPT**

-   **Dùng breakpoints**:

    1. DevTools > Sources panel
    2. Tìm file JS
    3. Click vào số dòng để đặt breakpoint
    4. Refresh trang
    5. Step qua từng dòng code

-   **Event không hoạt động**:
    1. Kiểm tra selectors
    2. Kiểm tra console errors
    3. Đảm bảo code chạy sau khi DOM đã load

## **📱 DEBUG MOBILE**

-   Dùng Device Mode trong Chrome (Ctrl+Shift+M)
-   Remote debug qua USB (chrome://inspect)
-   Test trên thiết bị thật khi có thể

## **🚨 LỖI THƯỜNG GẶP**

### **CSS**

-   Selector thiếu specificity (độ ưu tiên thấp)
-   Media queries không đúng
-   Typo trong class name
-   Flexbox/Grid không như mong đợi

### **JavaScript**

-   DOM chưa load xong khi code chạy
-   Sai selector khi query elements
-   Scope/this không đúng
-   Async code thiếu error handling

### **Network**

-   API endpoints không đúng
-   Request thiếu headers/params
-   CORS errors
-   Server response errors

## **🔍 CHECKLIST KHI DEBUG**

1. Console có lỗi không?
2. Network requests có thành công không?
3. DOM có đúng cấu trúc không?
4. CSS có áp dụng đúng không?
5. Event handlers có được kích hoạt không?
6. Mobile/responsive có vấn đề không?

## **⭐ TIP QUAN TRỌNG NHẤT**

**Từng bước một**: Debug là quá trình tìm tòi có phương pháp. Chia vấn đề thành từng phần nhỏ, theo dõi luồng dữ liệu, và kiểm tra từng giả thiết.

**Không đoán mò**: Dựa vào dữ liệu thực tế từ DevTools thay vì đoán, sẽ tiết kiệm thời gian hơn rất nhiều.

## **🛠️ Chrome DevTools**

Chrome DevTools là công cụ debug mạnh mẽ và không thể thiếu khi làm việc với frontend.

### **1. Elements Panel**

Dùng để kiểm tra và chỉnh sửa DOM, CSS:

-   **Inspect Element (Ctrl+Shift+C)**: Xem HTML và CSS của element
-   **Edit HTML**: Double-click vào element để chỉnh sửa trực tiếp
-   **Styles Pane**: Xem và chỉnh sửa CSS
-   **Computed Styles**: Xem styles đã tính toán sau khi áp dụng tất cả CSS
-   **Box Model**: Xem padding, border, margin của element
-   **Event Listeners**: Xem các event listeners gắn vào element

### **2. Console Panel**

Dùng để debug JavaScript:

-   **console.log()**: Hiển thị giá trị biến, object
-   **console.error()**: Hiển thị lỗi với màu đỏ
-   **console.warn()**: Hiển thị cảnh báo với màu vàng
-   **console.table()**: Hiển thị dữ liệu dạng bảng
-   **console.group()** và **console.groupEnd()**: Nhóm các logs lại với nhau

```javascript
// Ví dụ sử dụng console
console.log("User data:", userData);
console.error("API request failed:", error);

// Sử dụng console.table cho object/array
console.table(userList);

// Nhóm logs
console.group("API Request");
console.log("Request URL:", url);
console.log("Request Method:", method);
console.log("Request Data:", data);
console.groupEnd();
```

### **3. Network Panel**

Dùng để theo dõi network requests:

-   **Filter requests**: Lọc theo JS, CSS, XHR, etc.
-   **Throttling**: Mô phỏng network speeds chậm
-   **Headers**: Xem request và response headers
-   **Response**: Xem nội dung response
-   **Timing**: Phân tích thời gian của request

### **4. Performance Panel**

Dùng để phân tích hiệu suất:

-   **Record performance**: Ghi lại hoạt động của trang
-   **Analyze rendering**: Xem thời gian render và paint
-   **JavaScript execution**: Phân tích thời gian thực thi JS

### **5. Application Panel**

Dùng để kiểm tra storage:

-   **Local/Session Storage**: Xem và chỉnh sửa dữ liệu
-   **Cookies**: Quản lý cookies
-   **Cache**: Xem cache storage

## **🔄 Quy trình Debug Cơ bản**

### **1. Reproduce lỗi**

-   Xác định các bước để tái hiện lỗi
-   Ghi chú điều kiện xuất hiện lỗi (trình duyệt, thiết bị, etc.)
-   Tạo test case đơn giản nhất có thể

### **2. Xác định nguyên nhân**

-   Sử dụng DevTools để kiểm tra DOM, CSS và JavaScript
-   Kiểm tra Console để xem lỗi JavaScript
-   Sử dụng breakpoints trong JavaScript để theo dõi luồng thực thi
-   Kiểm tra Network panel để xem API requests

### **3. Fix lỗi**

-   Sửa code dựa trên nguyên nhân đã xác định
-   Test kỹ lưỡng sau khi sửa
-   Kiểm tra xem fix có gây ra side effects không

### **4. Refactor nếu cần thiết**

-   Xem xét cải thiện code để tránh lỗi tương tự trong tương lai
-   Cập nhật documentation nếu cần

## **🎯 Kỹ thuật Debug CSS**

### **1. Sử dụng Outline để debug layout**

```css
/* Thêm vào CSS khi debug layout */
* {
    outline: 1px solid red;
}

/* Hoặc chỉ debug một component cụ thể */
.fong-component * {
    outline: 1px solid blue;
}
```

### **2. Kiểm tra Specificity của CSS**

Khi CSS không được áp dụng như mong muốn, kiểm tra độ ưu tiên của selectors:

1. Mở DevTools > Elements panel
2. Chọn element cần kiểm tra
3. Xem Styles pane để hiểu tại sao một số styles bị ghi đè

### **3. Tìm và fix Responsive issues**

1. Sử dụng Device Mode trong DevTools (Ctrl+Shift+M)
2. Test ở nhiều kích thước màn hình
3. Kiểm tra các breakpoints media query
4. Xác định element gây overflow horizontal

## **💻 Kỹ thuật Debug JavaScript**

### **1. Sử dụng Breakpoints**

1. Mở DevTools > Sources panel
2. Tìm file JS cần debug
3. Click vào line number để đặt breakpoint
4. Refresh trang và thực hiện các bước để trigger code
5. Khi code dừng tại breakpoint, sử dụng Step Over, Step Into để theo dõi

### **2. Sử dụng Conditional Breakpoints**

Khi cần debug trong vòng lặp với điều kiện cụ thể:

1. Right-click vào line number
2. Chọn "Add conditional breakpoint"
3. Nhập condition (e.g., `index === 5`)

### **3. Debug Asynchronous Code**

```javascript
// Sử dụng async/await để debug dễ dàng hơn
async function fetchUserData() {
    try {
        console.log("Fetching data...");
        const response = await fetch("/api/users");
        console.log("Response status:", response.status);

        if (!response.ok) {
            throw new Error(`HTTP error: ${response.status}`);
        }

        const data = await response.json();
        console.log("Data received:", data);
        return data;
    } catch (error) {
        console.error("Fetch error:", error);
        throw error;
    }
}
```

## **📱 Debug trên Thiết bị Di động**

### **1. Remote Debugging với Chrome**

1. Kết nối thiết bị Android với máy tính qua USB
2. Bật USB debugging trên thiết bị
3. Trong Chrome, mở `chrome://inspect`
4. Chọn thiết bị và tab để debug

### **2. Sử dụng iOS Simulator**

1. Sử dụng Safari Web Inspector trên macOS
2. Connect tới iOS Simulator hoặc thiết bị thật

### **3. Tools Mô phỏng**

-   **BrowserStack**: Test trên nhiều thiết bị thật
-   **Responsively App**: Test responsive trên nhiều viewports cùng lúc

## **🚀 Kỹ thuật Performance Debugging**

### **1. Phân tích Render Performance**

1. Mở DevTools > Performance panel
2. Click Record
3. Thực hiện các tương tác trên trang
4. Dừng recording và phân tích kết quả
5. Tìm các Long Tasks và Jank

### **2. Tối ưu hóa CSS Rendering**

-   Tránh sử dụng quá nhiều shadows, gradients
-   Giảm số lượng CSS selectors phức tạp
-   Sử dụng `will-change` cho animations
-   Tránh layouts lồng nhau quá nhiều

### **3. Tối ưu hóa JavaScript Execution**

-   Tránh DOM manipulation quá nhiều
-   Sử dụng throttle và debounce cho event handlers
-   Lazy loading cho components không hiển thị ngay
-   Tránh blocking main thread với heavy computations

## **🔧 Công cụ Debugging khác**

### **1. Browser Extensions**

-   **React Developer Tools**: Debug React components
-   **Vue.js devtools**: Debug Vue components
-   **Redux DevTools**: Debug Redux state
-   **Augury**: Debug Angular applications

### **2. Logging Tools**

-   **Sentry**: Error tracking và monitoring
-   **LogRocket**: Session replay và error tracking

### **3. Performance Tools**

-   **Lighthouse**: Audit performance, accessibility, SEO
-   **WebPageTest**: Comprehensive performance testing

## **🧪 Unit Testing để Prevent Bugs**

### **1. Jest và Testing Library**

```javascript
// Ví dụ test cơ bản với Jest
test("button click increments counter", () => {
    // Setup
    document.body.innerHTML = `<button id="counter-btn">Click me</button>
                               <div id="counter">0</div>`;
    const btn = document.getElementById("counter-btn");
    const counter = document.getElementById("counter");

    // Attach event handler
    btn.addEventListener("click", () => {
        counter.textContent = parseInt(counter.textContent) + 1;
    });

    // Initial state
    expect(counter.textContent).toBe("0");

    // Act
    btn.click();

    // Assert
    expect(counter.textContent).toBe("1");
});
```

## **📋 Troubleshooting Checklist**

### **1. CSS Issues**

-   CSS không được applied:

    -   Kiểm tra file CSS đã được loaded chưa (Network panel)
    -   Kiểm tra specificity của selectors
    -   Kiểm tra typos trong class names
    -   Kiểm tra `!important` và inline styles

-   Responsive issues:
    -   Kiểm tra viewport meta tag
    -   Kiểm tra media queries
    -   Kiểm tra fixed width elements
    -   Kiểm tra overflow issues

### **2. JavaScript Issues**

-   JS không chạy:

    -   Kiểm tra Console để tìm errors
    -   Kiểm tra file JS đã được loaded chưa (Network panel)
    -   Kiểm tra DOM ready event
    -   Kiểm tra typos trong function names hoặc variables

-   Event handlers không hoạt động:
    -   Kiểm tra selectors
    -   Kiểm tra event delegation
    -   Kiểm tra scope của event handlers
    -   Kiểm tra timing của event binding

### **3. Network Issues**

-   API requests fails:
    -   Kiểm tra URL đúng không
    -   Kiểm tra parameters và headers
    -   Kiểm tra CORS issues
    -   Kiểm tra error responses từ server

## **📎 Debugging Helper trong Deutschfuns**

Deutschfuns có một helper đặc biệt cho việc debug JavaScript:

```javascript
// Sử dụng FongDebug helper (autoloaded globally)
FongDebug.log({
    label: "User Data",
    data: userData,
    fileName: "current-file.js",
});

// Log với chi tiết cụ thể và không gửi lên server
FongDebug.log({
    label: "Sensitive Info",
    data: sensitiveData,
    fileName: "user-profile.js",
    sendToServer: false,
});
```

## **📚 Tài liệu tham khảo**

-   [Chrome DevTools Documentation](https://developers.google.com/web/tools/chrome-devtools)
-   [MDN: JavaScript Debugging](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)
-   [CSS-Tricks: Debugging CSS](https://css-tricks.com/debugging-css/)
-   [Frontend Performance Checklist](https://www.smashingmagazine.com/2021/01/front-end-performance-2021-free-pdf-checklist/)

~ from global rules
