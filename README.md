💬 Real-time Chat Application with Spring Boot & WebSocket
"Spring Boot: Where enterprise meets elegance, turning complex Java development into a symphony of simplicity."
"Spring Boot: Nơi doanh nghiệp gặp gỡ sự tinh tế, biến việc phát triển Java phức tạp thành một bản giao hưởng của sự đơn giản."

📖 Project Overview
Welcome to a robust real-time chat application, built upon the powerful Spring Boot framework and WebSocket technology! This project delivers a seamless messaging experience, enabling multiple users to connect and interact within a single chat room. With its intuitive, user-friendly interface and instant update capabilities, it's the perfect solution for efficient group communication.

🛠️ Technologies Used
Backend
Java 17: The core programming language, ensuring high performance and stability.

Spring Boot 3.4.3: The leading framework, facilitating rapid and effortless application development.

Spring WebSocket: Provides real-time, bidirectional communication capabilities.

Spring Web: For building powerful RESTful web services.

Lombok: Significantly reduces boilerplate code, leading to cleaner and more readable codebases.

STOMP (Simple Text Oriented Messaging Protocol): An efficient and straightforward messaging protocol over WebSocket.

Frontend
HTML5: Modern web page structure.

CSS3: Styling and ensuring responsive design across all devices.

JavaScript ES6: Client-side logic, delivering dynamic and interactive user experiences.

SockJS: A WebSocket fallback library, ensuring stable connections even in restrictive network environments.

STOMP.js: A JavaScript client for the STOMP protocol, simplifying message sending and receiving.

Build Tools
Maven 3.9.9: Dependency management and build automation tool.

Maven Wrapper: Ensures all developers use the same Maven version, preventing compatibility issues.

🚀 Setup & Running Instructions
System Requirements
Java 17 or higher.

Maven 3.6+ (or utilize the Maven Wrapper included in the project).

IDE: VS Code or IntelliJ IDEA are highly recommended.

🔧 Setup with VS Code
Clone repository:

git clone <repository-url>
cd chat-application

Install Essential Extensions:

Extension Pack for Java

Spring Boot Extension Pack

Lombok Annotations Support for VS Code

Open project:

code .

Run the application:

Open Terminal in VS Code (Ctrl + `).

Execute command: ./mvnw spring-boot:run

Alternatively, use the Command Palette (Ctrl+Shift+P) and search for "Spring Boot: Run".

🔧 Setup with IntelliJ IDEA
Import project:

File → Open → Select the project directory.

IntelliJ will automatically detect the Maven project.

Configure Lombok:

File → Settings → Plugins → Search and install "Lombok".

File → Settings → Build, Execution, Deployment → Compiler → Annotation Processors → Check Enable annotation processing.

Run the application:

Option 1: Click on the ChatApplication class → Run.

Option 2: Open Maven panel → Plugins → spring-boot → spring-boot:run.

Option 3: Open Terminal → ./mvnw spring-boot:run.

🌐 Accessing the Application
Once the application has successfully launched, open your web browser and navigate to:

http://localhost:8080

📁 Project Structure
src/
├── main/
│   ├── java/com/marcus/chat/
│   │   ├── ChatApplication.java          # Main application class
│   │   ├── chat/
│   │   │   ├── ChatController.java       # WebSocket message handlers
│   │   │   ├── ChatMessage.java          # Message data model
│   │   │   └── MessageType.java          # Message type enum
│   │   └── config/
│   │       ├── WebSocketConfig.java      # WebSocket configuration
│   │       └── WebSocketEventListener.java # WebSocket event listener
│   └── resources/
│       ├── static/
│       │   ├── css/main.css             # Stylesheet for the UI
│       │   ├── js/app.js                # Client-side JavaScript
│       │   └── index.html               # Main HTML page
│       └── application.properties        # Application configuration file
└── test/
    └── java/com/marcus/chat/
        └── ChatApplicationTests.java     # Unit tests

🎯 Key Features
✅ Real-time Messaging: Messages are sent and received instantly, providing a seamless chat experience.

✅ Multi-user Support: Accommodates multiple users concurrently within a single chat room.

✅ User Join/Leave Notifications: Clear notifications when users join or leave the chat room.

✅ Timestamp Display: Detailed display of message timestamps.

✅ Avatar Colors: Automatic assignment of avatar colors based on usernames, aiding easy identification.

✅ Responsive Design: The interface is optimized for beautiful display and smooth operation on all screen sizes (desktop, tablet, mobile).

✅ Connection Status: Displays the WebSocket connection status, letting users know when they are online.

🔧 Configuration
Server Port
By default, the application runs on port 8080. To change it, modify the application.properties file:

server.port=8081

WebSocket Endpoints
STOMP Endpoint: /ws

Application Destination Prefix: /app

Topic Prefix: /topic

Public Chat Topic: /topic/public

🎮 How to Use
Access the application: Open your browser and go to http://localhost:8080.

Enter your name: Type your username into the input field and click "Start Chatting".

Chat: Type your message into the input box and press Enter or click the "Send" button.

Exit: Close the browser tab or window to disconnect.

💡 Tip: To test multi-user functionality, open multiple browser tabs and log in with different usernames!

🧪 Testing
Running Tests
./mvnw test

Or within your IDE:

VS Code: Command Palette → "Java: Run Tests"

IntelliJ IDEA: Right-click on the test class → "Run Tests"

📦 Build and Deploy
Build JAR file
./mvnw clean package

Run JAR file
java -jar target/chat-0.0.1-SNAPSHOT.jar

🛠️ Troubleshooting
Common Issues
Port already in use:

Error: Port 8080 is already in use

Solution: Change the port in application.properties or find and terminate the process using port 8080.

Lombok not working:

Ensure you have installed the Lombok plugin for your IDE.

Check and enable annotation processing in your IDE settings.

WebSocket connection failed:

Check your firewall or proxy settings.

Ensure your browser supports WebSocket.

👨‍💻 Author
QuangCaptain - Initial project contributor.

📄 License
This project is licensed under the Apache License 2.0.

🤝 Contributing
We welcome all contributions to improve this project!

Fork the project.

Create your feature branch (git checkout -b feature/AmazingFeature).

Commit your changes (git commit -m 'Add some AmazingFeature').

Push to the branch (git push origin feature/AmazingFeature).

Open a Pull Request.
