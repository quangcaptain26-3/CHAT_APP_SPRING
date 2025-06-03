# 💬 Spring Boot WebSocket Chat Application

> *"Spring Boot - Where enterprise meets elegance, turning complex Java development into a symphony of simplicity."*

## 📖 Mô tả dự án

Ứng dụng chat real-time được xây dựng với Spring Boot và WebSocket, cho phép nhiều người dùng trò chuyện trong cùng một phòng chat. Giao diện đơn giản, thân thiện với người dùng và hỗ trợ thời gian thực.

## 🛠️ Công nghệ sử dụng

### Backend
- **Java 17** - Ngôn ngữ lập trình chính
- **Spring Boot 3.4.3** - Framework chính
- **Spring WebSocket** - Hỗ trợ WebSocket cho real-time messaging
- **Spring Web** - RESTful web services
- **Lombok** - Giảm boilerplate code
- **STOMP** (Simple Text Oriented Messaging Protocol) - Messaging protocol

### Frontend
- **HTML5** - Cấu trúc trang web
- **CSS3** - Styling và responsive design
- **JavaScript ES6** - Logic phía client
- **SockJS** - WebSocket fallback library
- **STOMP.js** - STOMP client for JavaScript

### Build Tools
- **Maven 3.9.9** - Dependency management và build automation
- **Maven Wrapper** - Đảm bảo version consistency

## 🚀 Hướng dẫn cài đặt và chạy

### Yêu cầu hệ thống
- Java 17 hoặc cao hơn
- Maven 3.6+ (hoặc sử dụng Maven Wrapper có sẵn)
- IDE: VS Code hoặc IntelliJ IDEA

### 🔧 Cài đặt với VS Code

1. **Clone repository:**
   ```bash
   git clone <repository-url>
   cd chat-application
   ```

2. **Cài đặt extensions cần thiết:**
   - Extension Pack for Java
   - Spring Boot Extension Pack
   - Lombok Annotations Support for VS Code

3. **Mở project:**
   ```bash
   code .
   ```

4. **Chạy ứng dụng:**
   - Mở Terminal trong VS Code (`Ctrl + `)
   - Chạy lệnh:
     ```bash
     ./mvnw spring-boot:run
     ```
   - Hoặc sử dụng Command Palette (`Ctrl+Shift+P`) và tìm "Spring Boot: Run"

### 🔧 Cài đặt với IntelliJ IDEA

1. **Import project:**
   - File → Open → Chọn thư mục chứa project
   - IntelliJ sẽ tự động detect Maven project

2. **Cấu hình Lombok:**
   - File → Settings → Plugins → Tìm và cài đặt "Lombok"
   - File → Settings → Build → Compiler → Annotation Processors → Enable annotation processing

3. **Chạy ứng dụng:**
   - Cách 1: Click vào class `ChatApplication` → Run
   - Cách 2: Maven panel → Plugins → spring-boot → spring-boot:run
   - Cách 3: Terminal → `./mvnw spring-boot:run`

### 🌐 Truy cập ứng dụng

Sau khi chạy thành công, mở trình duyệt và truy cập:
```
http://localhost:8080
```

## 📁 Cấu trúc dự án

```
src/
├── main/
│   ├── java/com/marcus/chat/
│   │   ├── ChatApplication.java          # Main application class
│   │   ├── chat/
│   │   │   ├── ChatController.java       # WebSocket message handlers
│   │   │   ├── ChatMessage.java          # Message model
│   │   │   └── MessageType.java          # Message type enum
│   │   └── config/
│   │       ├── WebSocketConfig.java      # WebSocket configuration
│   │       └── WebSocketEventListener.java # Event listener
│   └── resources/
│       ├── static/
│       │   ├── css/main.css             # Stylesheet
│       │   ├── js/app.js                # Client-side JavaScript
│       │   └── index.html               # Main HTML page
│       └── application.properties        # Configuration file
└── test/
    └── java/com/marcus/chat/
        └── ChatApplicationTests.java     # Unit tests
```

## 🎯 Tính năng chính

- ✅ **Real-time messaging** - Tin nhắn được gửi và nhận ngay lập tức
- ✅ **Multi-user support** - Hỗ trợ nhiều người dùng cùng lúc
- ✅ **User join/leave notifications** - Thông báo khi có người tham gia/rời khỏi
- ✅ **Timestamp display** - Hiển thị thời gian gửi tin nhắn
- ✅ **Avatar colors** - Màu avatar tự động dựa trên tên người dùng
- ✅ **Responsive design** - Giao diện thích ứng với mọi thiết bị
- ✅ **Connection status** - Hiển thị trạng thái kết nối

## 🔧 Cấu hình

### Cổng server
Mặc định ứng dụng chạy trên cổng `8080`. Để thay đổi, sửa file `application.properties`:
```properties
server.port=8081
```

### WebSocket endpoints
- **STOMP endpoint:** `/ws`
- **Application destination prefix:** `/app`
- **Topic prefix:** `/topic`
- **Public chat topic:** `/topic/public`

## 🎮 Cách sử dụng

1. **Truy cập ứng dụng:** Mở `http://localhost:8080`
2. **Nhập tên:** Gõ username và click "Start Chatting"
3. **Chat:** Gõ tin nhắn và nhấn Enter hoặc click "Send"
4. **Thoát:** Đóng tab/cửa sổ trình duyệt

## 🧪 Testing

Chạy tests:
```bash
./mvnw test
```

Hoặc trong IDE:
- **VS Code:** Command Palette → "Java: Run Tests"
- **IntelliJ:** Right-click trên test class → "Run Tests"

## 📦 Build và Deploy

### Build JAR file:
```bash
./mvnw clean package
```

### Chạy JAR file:
```bash
java -jar target/chat-0.0.1-SNAPSHOT.jar
```

## 🛠️ Troubleshooting

### Lỗi thường gặp:

1. **Port đã được sử dụng:**
   ```
   Error: Port 8080 is already in use
   ```
   **Giải pháp:** Đổi port trong `application.properties` hoặc kill process đang dùng port 8080

2. **Lombok không hoạt động:**
   - Đảm bảo đã cài đặt Lombok plugin
   - Enable annotation processing trong IDE

3. **WebSocket connection failed:**
   - Kiểm tra firewall/proxy settings
   - Đảm bảo browser hỗ trợ WebSocket

## 👨‍💻 Tác giả

**QuangCaptain** - *Initial work*

## 📄 License

This project is licensed under the Apache License 2.0

## 🤝 Đóng góp

1. Fork project
2. Tạo feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Tạo Pull Request

---

💡 **Tip:** Để test với nhiều người dùng, mở nhiều tab trình duyệt với các username khác nhau!
