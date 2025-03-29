<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Khu Tự Trị</title>
    
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: white;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
        }

        .story img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Link ảnh minh họa đầu tiên -->
        <img src="doraemon.jpg" alt="Ảnh 1">

        <!-- Link ảnh minh họa thứ hai -->
        <img src="meo.jpg" alt="Ảnh 2">

        <!-- Thêm nhiều ảnh nếu cần -->
        <img src="th.jpg" alt="Ảnh 3">
    </div>
</body>
</html>
<%@ page contentType="text/html; charset=UTF-8" %>
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Chat</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        .chat-container {
            width: 350px;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            display: flex;
            flex-direction: column;
        }
        .chat-box {
            height: 300px;
            border: 1px solid #ccc;
            overflow-y: auto;
            padding: 10px;
            background: #fff;
            border-radius: 5px;
        }
        .input-box {
            display: flex;
            margin-top: 10px;
        }
        input {
            flex: 1;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            padding: 10px;
            background: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            margin-left: 5px;
            cursor: pointer;
        }
        button:hover {
            background: #0056b3;
        }
    </style>
</head>
<body>

<div class="chat-container">
    <h2>Chat Đơn Giản</h2>
    <div class="chat-box" id="chatBox">
        <!-- Tin nhắn sẽ hiển thị ở đây -->
    </div>
    <div class="input-box">
        <input type="text" id="messageInput" placeholder="Nhập tin nhắn...">
        <button onclick="sendMessage()">Gửi</button>
    </div>
</div>

<script>
    function sendMessage() {
        let input = document.getElementById("messageInput");
        let message = input.value.trim();
        if (message === "") return;

        let chatBox = document.getElementById("chatBox");
        
        // Tạo một thẻ div để hiển thị tin nhắn
        let msgDiv = document.createElement("div");
        msgDiv.textContent = "Bạn: " + message;
        msgDiv.style.padding = "5px";
        msgDiv.style.margin = "5px 0";
        msgDiv.style.borderRadius = "5px";
        msgDiv.style.backgroundColor = "#e1f5fe";

        // Thêm tin nhắn vào hộp chat
        chatBox.appendChild(msgDiv);
        chatBox.scrollTop = chatBox.scrollHeight; // Cuộn xuống tin nhắn mới nhất

        // Xóa nội dung ô nhập tin nhắn
        input.value = "";
    }
</script>

</body>
</html>

