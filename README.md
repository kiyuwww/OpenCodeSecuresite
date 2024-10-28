<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Winzly's Social Networks</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Reset default margins and paddings */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Body styling */
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #121212;
            font-family: Arial, sans-serif;
            color: #fff;
        }

        /* Container styling */
        .container {
            text-align: center;
            padding: 20px;
            opacity: 0;
            transform: translateY(-50px);
            animation: slideIn 1s forwards;
        }

        /* Social links styling */
        .social-links {
            margin-top: 20px;
            opacity: 0;
            transform: translateX(-50px);
            animation: slideInIcons 1s 0.5s forwards;
        }

        .social-links a {
            color: #fff;
            text-decoration: none;
            font-size: 3rem;
            margin: 0 15px;
            transition: transform 0.3s ease, color 0.3s;
        }

        .social-links a:hover {
            transform: scale(1.2);
            color: #000; /* Change color to black on hover */
        }

        /* Support button styling */
        .support-button {
            position: absolute;
            top: 20px;
            right: 20px;
            background-color: #1e90ff;
            color: #fff;
            padding: 10px 20px;
            font-size: 1rem;
            font-weight: bold;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .support-button:hover {
            background-color: #0f78d1;
        }

        /* Copy success message styling */
        .copy-message {
            position: absolute;
            top: 60px;
            right: 20px;
            background-color: #4CAF50;
            color: #fff;
            padding: 10px;
            border-radius: 5px;
            font-size: 0.9rem;
            opacity: 0;
            transform: translateX(100%);
            transition: opacity 0.3s ease, transform 0.3s ease;
        }

        .copy-message.show {
            opacity: 1;
            transform: translateX(0);
        }

        /* Keyframes for slide-in animations */
        @keyframes slideIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideInIcons {
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>MY BIO</h1>
        <div class="social-links">
            <a href="https://www.twitch.tv/winzly_" target="_blank" aria-label="Twitch"><i class="fab fa-twitch"></i></a>
            <a href="https://dsc.gg/winzly" target="_blank" aria-label="Discord"><i class="fab fa-discord"></i></a>
        </div>
    </div>
    <button class="support-button" onclick="copyDiscordNickname()">Support</button>
    <div class="copy-message" id="copyMessage">Copied .winzly to clipboard!</div>

    <script>
        function copyDiscordNickname() {
            const nickname = '.winzly';
            navigator.clipboard.writeText(nickname).then(() => {
                const message = document.getElementById('copyMessage');
                message.classList.add('show');
                setTimeout(() => {
                    message.classList.remove('show');
                }, 2000); // Show message for 2 seconds
            }).catch(err => {
                console.error('Could not copy text: ', err);
            });
        }
    </script>
</body>
</html>
