<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ChatGPT Web Interface</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f4f4f4;
        }
        #chat-container {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 500px;
            width: 100%;
        }
        #messages {
            height: 300px;
            overflow-y: auto;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            padding: 10px;
            border-radius: 5px;
            background-color: #fafafa;
        }
        .message {
            margin: 10px 0;
        }
        .message.user {
            text-align: right;
        }
        input[type="text"], button {
            padding: 10px;
            font-size: 16px;
            border-radius: 5px;
        }
        input[type="text"] {
            width: 75%;
            border: 1px solid #ccc;
        }
        button {
            width: 20%;
            border: none;
            background-color: #007BFF;
            color: white;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div id="chat-container">
        <div id="messages"></div>
        <input type="text" id="user-input" placeholder="Type your message here...">
        <button id="send-btn">Send</button>
    </div>

    <script>
        const messagesDiv = document.getElementById('messages');
        const userInput = document.getElementById('user-input');
        const sendBtn = document.getElementById('send-btn');

        // Function to display messages in the chat
        function displayMessage(message, sender) {
            const messageDiv = document.createElement('div');
            messageDiv.classList.add('message', sender);
            messageDiv.textContent = message;
            messagesDiv.appendChild(messageDiv);
            messagesDiv.scrollTop = messagesDiv.scrollHeight; // Scroll to bottom
        }

        // Function to handle sending the message
        async function sendMessage() {
            const userMessage = userInput.value.trim();
            if (!userMessage) return;

            displayMessage(userMessage, 'user'); // Display user message

            // Clear input
            userInput.value = '';

            // Call ChatGPT API (replace this with your actual API call)
            try {
                const response = await fetch('https://api.openai.com/v1/chat/completions', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json',
                        'Authorization': `Bearer YOUR_API_KEY` // replace with your API key
                    },
                    body: JSON.stringify({
                        model: "gpt-3.5-turbo",
                        messages: [{ role: "user", content: userMessage }]
                    })
                });

                const data = await response.json();
                const botMessage = data.choices[0].message.content;
                displayMessage(botMessage, 'bot'); // Display bot response
            } catch (error) {
                displayMessage("Error: Unable to connect to ChatGPT.", 'bot');
            }
        }

        sendBtn.addEventListener('click', sendMessage);

        // Send message on Enter key press
        userInput.addEventListener('keydown', (e) => {
            if (e.key === 'Enter') sendMessage();
        });
    </script>
</body>
</html>
