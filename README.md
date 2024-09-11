<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home</title>
	    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            font-family: "Lato", sans-serif;
        }
        .sidenav {
            height: 100%;
            width: 250px;
            position: fixed;
            z-index: 1;
            top: 0;
            left: 0;
            background-color: #111;
            overflow-x: hidden;
            padding-top: 20px;
        }
        .sidenav a {
            padding: 8px 8px 8px 16px;
            text-decoration: none;
            font-size: 25px;
            color: #818181;
            display: block;
            transition: 0.3s;
        }
        .sidenav a:hover {
            color: #f1f1f1;
        }
        .main {
            margin-left: 260px;
			padding-top: 0.01px;
        }
    </style>
<style>
.vertical-line {
  border-left: 15px solid black;
	border-right: 15px solid black;
  height: 1px;
  background-color: white;
}
</style>
<style>
buton{
	displal: flex;
	border-right: 15px;
	border-left: 15px
	border-top: 15px;
	width: 100px;
	height: 30px;
	border-radius: 10px;
	box-shadow: 0px 1px 10px black;
	background-color: white;
	font-size: 20px;
	color: black;
	padding-top: 25px;
	padding-left: 5px;
	padding-right: 5px;
	padding-bottom: 2px;
}	
buton a:hover{
	background-color: white;
	color: #98F5F9;
}
</style>
<style>
        button {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
			border-radius: 10px;
	        box-shadow: 0px 1px 10px #4CAF49;	
        }
        button:hover {
            background-color: #45a049;
        }
</style>
<style>
        body {
            font-family: Arial, sans-serif;
        }
        .chat-container {
            width: 100%;
			height: 100%;
            margin: 50px auto;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
			float: left;
        }
        .chat-header {
            background-color: #007bff;
            color: #fff;
            padding: 15px 1200px 15px 15px;
            text-align: center;
			float: left;
        }
        .chat-messages {
            padding: 34px;
            height: 400px;
            overflow-y: scroll;
			padding-top: 100px;
			color: black;
        }
        .message {
            margin-bottom: 15px;
            position: relative;
        }
        .message p {
            margin: 0;
        }
        .message .time {
            font-size: 0.8em;
            color: #888;
        }
        .delete-button {
            position: absolute;
            top: 5px;
            right: 5px;
            background-color: red;
            color: white;
            border: none;
            cursor: pointer;
            padding: 5px;
            border-radius: 8px;
        }
        .chat-input {
            display: flex;
            border-top: 1px solid #ddd;
			border-radius: 8px;
        }
        .chat-input input {
            flex: 1;
            padding: 15px;
            border: none;
            border-radius: 8;
        }
        .chat-input button {
            padding: 15px;
            background-color: #007bff;
            color: #fff;
            border: none;
            cursor: pointer;
			border-radius: 8px;
        }
    </style>
</head>
<body>
<div class="sidenav">
	<h1><font color="blue"><u><font style="  border-left: 25px solid black;">MENU</u></font></h1>
	<p></p>
    <a href="file:///C:/Users/user/Desktop/3.html"><font color="white">Home.<i class="fa fa-home" aria-hidden="true" style="font-size:35px;color:white;"></i></a>
	<font color="white"><div class="vertical-line"></div>
    <a href="file:///C:/Users/user/Desktop/7.html">Sign In.<i class="fa fa-id-card" aria-hidden="true" style="font-size:35px;color:white;"></i></a>
	<font color="white"><div class="vertical-line"></div>
    <a href="file:///C:/Users/user/Desktop/8.html">Contact.<i class="fa fa-question-circle" aria-hidden="true"style="font-size:35px;color:white;"></i></a>
	<font color="white"><div class="vertical-line"></div>
</div>
<div class="main">
    <div class="chat-container">
        <div class="chat-header">
        <i class="fa fa-info-circle" aria-hidden="true" style="font-size:50px;color:white;">.Messages</i>
        </div>
        <div class="chat-messages" id="chat-messages">
        </div>
        <div class="chat-input">
            <input type="text" id="message-input" placeholder="Type a message..." border-radius="8px">
            <button onclick="sendMessage()"><i class="fa fa-paper-plane" aria-hidden="true"></i></button>
        </div>
    </div>
    <script>
        // Load messages from local storage
        const chatMessages = document.getElementById('chat-messages');
        let savedMessages = JSON.parse(localStorage.getItem('chatMessages')) || [];
        savedMessages.forEach((message, index) => {
            displayMessage(message, index);
        });
        // Function to display a message
        function displayMessage(message, index) {
            const messageElement = document.createElement('div');
            messageElement.classList.add('message');
            messageElement.innerHTML = `<p><strong>You:</strong> ${message.text}</p><p class="time">${message.time}</p><button class="delete-button" onclick="deleteMessage(this, ${index})">Delete</button>`;
            chatMessages.appendChild(messageElement);
        }
        function sendMessage() {
            const input = document.getElementById('message-input');
            const messageText = input.value.trim();
            if (messageText) {
                const message = {
                    text: messageText,
                    time: new Date().toLocaleTimeString()
                };
                // Display the message
                displayMessage(message, savedMessages.length);
                // Save the message to local storage
                savedMessages.push(message);
                localStorage.setItem('chatMessages', JSON.stringify(savedMessages));
                // Clear the input
                input.value = '';
                chatMessages.scrollTop = chatMessages.scrollHeight;
            }
        }
        // Function to delete a message
        function deleteMessage(button, index) {
            savedMessages.splice(index, 1);
            localStorage.setItem('chatMessages', JSON.stringify(savedMessages));
            chatMessages.innerHTML = '';
            savedMessages.forEach((message, index) => {
                displayMessage(message, index);
            });
        }
    </script>   
</div>
</body>
</html>
