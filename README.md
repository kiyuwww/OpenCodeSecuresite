<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Winzly Profile</title>
    <!-- Подключаем Font Awesome для иконок -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #121212;
            color: #fff;
            position: relative;
            flex-direction: column;
            text-align: center;
            overflow: hidden;
        }

        .container {
            max-width: 800px;
            width: 100%;
            padding: 20px;
            opacity: 0;
            animation: fadeIn 0.7s forwards 0.2s;
        }

        @keyframes fadeIn {
            0% {
                opacity: 0;
            }
            100% {
                opacity: 1;
            }
        }

        .welcome-message h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            animation: slideIn 0.7s ease-out forwards;
        }

        @keyframes slideIn {
            0% {
                transform: translateX(100%);
            }
            100% {
                transform: translateX(0);
            }
        }

        .sub-message {
            font-size: 1.5rem;
            margin-bottom: 30px;
            animation: slideIn 1s ease-out forwards;
        }

        .discord-button {
            background-color: #5865F2;
            color: #fff;
            border: none;
            padding: 10px 20px;
            font-size: 1rem;
            border-radius: 5px;
            cursor: pointer;
            position: absolute;
            top: 20px;
            right: 20px;
            opacity: 0;
            animation: slideInButton 1s ease-out forwards;
        }

        @keyframes slideInButton {
            0% {
                transform: translateY(50%);
            }
            100% {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .notification {
            position: absolute;
            top: 70px;
            right: 20px;
            background-color: #333;
            color: #fff;
            padding: 10px 20px;
            border-radius: 5px;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .notification.visible {
            opacity: 1;
        }

        .notification.hidden {
            opacity: 0;
        }

        /* Стиль для блока социальных сетей */
        .social-links-container {
            margin-top: 40px;
            animation: slideInIcons 1.5s ease-out forwards;
        }

        @keyframes slideInIcons {
            0% {
                transform: translateY(100%);
            }
            100% {
                transform: translateY(0);
            }
        }

        .social-links {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .social-item {
            display: flex;
            align-items: center;
            background-color: #1f1f1f;
            border: 2px solid #fff;
            padding: 10px 20px;
            border-radius: 10px;
            margin: 10px;
            transition: background-color 0.3s ease, transform 0.3s ease;
            max-width: 300px;
        }

        .social-item:hover {
            background-color: #5865F2;
            transform: scale(1.05);
        }

        .social-item i {
            font-size: 2.5rem;
            margin-right: 15px; /* Отступ между иконкой и текстом */
        }

        .social-item p {
            font-size: 1.2rem;
            color: #fff;
            margin: 0;
        }

        .social-links-container h2 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #fff;
            font-weight: 600;
        }

    </style>
</head>
<body>
    <div class="container">
        <div class="welcome-message">
            <h1>Welcome to my Winzly profile</h1>
        </div>
        <div class="sub-message">
            <p>Check out my gaming abilities, projects, and feel free to connect!</p>
        </div>
        <button class="discord-button" onclick="copyToClipboard()">Discord</button>
        <div id="notification" class="notification hidden">Text ".winzly" copied!</div>

        <div class="social-links-container">
            <h2>Social Networks</h2>
            <div class="social-links">
                <!-- Иконки социальных сетей с Font Awesome -->
                <div class="social-item">
                    <i class="fab fa-twitch"></i>
                    <p>Twitch</p>
                </div>
                <div class="social-item">
                    <i class="fab fa-steam"></i>
                    <p>Steam</p>
                </div>
                <div class="social-item">
                    <i class="fab fa-vk"></i>
                    <p>VK</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        function copyToClipboard() {
            const textToCopy = ".winzly";
            navigator.clipboard.writeText(textToCopy).then(() => {
                const notification = document.getElementById("notification");
                notification.classList.remove("hidden");
                notification.classList.add("visible");

                setTimeout(() => {
                    notification.classList.remove("visible");
                    notification.classList.add("hidden");
                }, 1500);
            });
        }
    </script>
</body>
</html>
