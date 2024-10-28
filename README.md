<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Social Networks</title>
    <style>
        body {
            background-color: black;
            color: white;
            display: flex;
            justify-content: flex-start;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            margin: 0;
            overflow: hidden;
        }
        .content {
            animation: slideIn 2s ease-out;
            text-align: center;
        }
        .social-icons {
            margin-top: 20px;
            animation: slideIn 2s ease-out;
        }
        .social-icons a {
            margin: 0 15px;
        }
        .social-icons img {
            width: 50px;
            height: 50px;
            transition: filter 0.3s;
        }
        .social-icons img:hover {
            filter: invert(100%);
        }
        .support-button {
            position: absolute;
            top: 20px;
            right: 20px;
            padding: 10px 20px;
            background-color: grey;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            cursor: pointer;
            animation: slideIn 2s ease-out;
        }
        .support-button:hover {
            background-color: darkgrey;
        }
        .notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: green;
            color: white;
            padding: 10px;
            border-radius: 5px;
            display: none;
        }
        @keyframes slideIn {
            from {
                transform: translateY(100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
    </style>
    <script>
        function copyToClipboard() {
            const textToCopy = ".winzly";
            navigator.clipboard.writeText(textToCopy).then(() => {
                showNotification();
            });
        }

        function showNotification() {
            const notification = document.getElementById('notification');
            notification.style.display = 'block';
            setTimeout(() => {
                notification.style.display = 'none';
            }, 3000);
        }
    </script>
</head>
<body>
    <div class="content">
        <h1>MY BIO</h1>
        <div class="social-icons">
            <a href="https://dsc.gg/winzly" target="_blank">
                <img src="discord-icon.png" alt="Discord">
            </a>
            <a href="https://www.twitch.tv/winzly_" target="_blank">
                <img src="twitch-icon.png" alt="Twitch">
            </a>
        </div>
    </div>
    <div class="support-button" onclick="copyToClipboard()">Support</div>
    <div id="notification" class="notification">Discord nickname copied: .winzly</div>
</body>
</html>
