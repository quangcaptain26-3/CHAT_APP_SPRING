# 💬 Spring Boot WebSocket Chat Application

> *"Spring Boot is where Java speaks the language of the future — fast, elegant, and built to scale."*
> 
> **Spring Boot 是Java说话未来的地方，快速、优雅，并且具有伸缩性。**
> 
> **Spring Boot là nơi Java nói ngôn ngữ của tương lai — nhanh chóng, thanh thoát và dễ mở rộng.**

## 📖 Mô tả dự án

Ứng dụng chat real-time được xây dựng với Spring Boot và WebSocket, cho phép nhiều người dùng trò chuyện trong cùng một phòng chat. Giao diện đơn giản, thân thiện và hỗ trợ thời gian thực.

## 🛠️ Công nghệ sử dụng

### Backend

* **Java 17**
* **Spring Boot 3.4.3**
* **Spring WebSocket**
* **Spring Web**
* **Lombok**
* **STOMP** (Simple Text Oriented Messaging Protocol)

### Frontend

* **HTML5**, **CSS3**, **JavaScript ES6**
* **SockJS**
* **STOMP.js**

### Build Tools

* **Maven 3.9.9**
* **Maven Wrapper**

## 🚀 Hướng dẫn cài đặt và chạy

Chi tiết hướng dẫn cho VS Code và IntelliJ IDEA đã được cung cấp đầy đủ (clone, run, test, etc.).

## 📁 Cấu trúc dự án

```
src/
├── main/java/com/marcus/chat/
│   ├── ChatApplication.java
│   ├── chat/
│   │   ├── ChatController.java
│   │   ├── ChatMessage.java
│   │   └── MessageType.java
│   └── config/
│       ├── WebSocketConfig.java
│       └── WebSocketEventListener.java
├── resources/
│   ├── static/
│   │   ├── css/main.css
│   │   ├── js/app.js
│   │   └── index.html
│   └── application.properties
└── test/java/com/marcus/chat/
    └── ChatApplicationTests.java
```

## 🎯 Tính năng chính

* ✅ Nhắn tin thời gian thực
* ✅ Hỗ trợ nhiều người dùng
* ✅ Thông báo tham gia/rời khỏi
* ✅ Hiển thị thời gian
* ✅ Avatar theo tên người dùng
* ✅ Responsive UI
* ✅ Trạng thái kết nối

## 🔧 Cấu hình

**Port:** `server.port=8080` (hoặc thay đổi trong `application.properties`)

**WebSocket endpoints:**

* STOMP endpoint: `/ws`
* Prefix app: `/app`
* Topic: `/topic/public`

## 🎮 Cách sử dụng

1. Truy cập `http://localhost:8080`
2. Nhập username
3. Gửi tin nhắn
4. Đóng tab để thoát

## 🧪 Testing

```bash
./mvnw test
```

## 📦 Build & Deploy

```bash
./mvnw clean package
java -jar target/chat-0.0.1-SNAPSHOT.jar
```

## 🚧 Troubleshooting

1. **Port bị trùng:** Đổi port
2. **Lombok không hoạt động:** Cài plugin + Bật annotation processing
3. **WebSocket lỗi:** Kiểm tra firewall/proxy

## 👨‍💼 Tác giả

**QuangCaptain** - *Initial work*

## 📄 License

Apache License 2.0

## 🤝 Đóng góp

1. Fork project
2. Tạo feature branch (git checkout -b feature/AmazingFeature)
3.  Commit changes (git commit -m 'Add some AmazingFeature')
4.  Push to branch (git push origin feature/AmazingFeature)
5.  Tạo Pull Request

---

💡 **Mẹo:** Để test với nhiều người, hãy mở nhiều tab với các username khác nhau!
