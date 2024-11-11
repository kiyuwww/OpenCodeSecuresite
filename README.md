<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Support Button</title>
    <!-- Подключаем Font Awesome для иконок -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" rel="stylesheet">
    <!-- Добавляем красивый шрифт из Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #000; /* Черный фон */
            font-family: Arial, sans-serif;
            color: #fff; /* Белый цвет текста */
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            height: 100vh;
            position: relative;
            overflow: hidden;
        }

        /* Центрированный текст */
        .center-text {
            font-size: 36px;
            font-weight: bold;
            color: #fff; /* Белый цвет текста */
            position: absolute;
            top: 35%; /* Текст выше */
            left: 50%;
            transform: translateX(-50%);
            font-family: 'Roboto Slab', serif;
            text-align: center;
            z-index: 1;
            transition: all 0.5s ease-out; /* Анимация для подъема */
        }

        /* Кнопка Support в правом верхнем углу */
        .support-btn {
            background-color: #fff; /* Белый фон */
            border: 2px solid #333; /* Черная рамка */
            color: #333; /* Черный текст */
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            position: absolute;
            top: 20px;
            right: 20px;
            font-weight: bold; /* Жирный шрифт */
            transition: all 0.3s ease;
        }

        .support-btn:hover {
            background-color: #333; /* Черный фон при наведении */
            color: #fff; /* Белый текст при наведении */
        }

        /* Сообщение об успешном копировании */
        .copy-message {
            display: none;
            color: #fff;
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
            animation: fadeIn 2s ease-out;
            text-align: center;
        }

        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }

        /* Стиль для иконок социальных сетей */
        .social-icons {
            margin-top: 40px;
            display: flex;
            justify-content: center;
            gap: 20px;
            opacity: 0;
            animation: slideUp 1s forwards;
            padding: 10px;
            border: 2px solid #ccc;
            border-radius: 8px;
            background-color: #222; /* Темный фон для блока с иконками */
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        @keyframes slideUp {
            0% {
                transform: translateY(50px);
                opacity: 0;
            }
            100% {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .social-icons a {
            color: #fff; /* Белый цвет иконок */
            font-size: 24px;
            text-decoration: none;
            transition: color 0.3s, background-color 0.3s;
            padding: 8px;
            border-radius: 50%;
        }

        .social-icons a:hover {
            color: #000; /* Черный цвет текста при наведении */
            background-color: #fff; /* Белый фон при наведении */
        }

    </style>
</head>
<body>
    <!-- Центрированный текст -->
    <div class="center-text" id="centerText">Winzly's setup</div>

    <button id="supportButton" class="support-btn">Support</button>

    <div class="container">
        <div id="copyMessage" class="copy-message">Discord has been copied!</div>
    </div>

    <div class="social-icons">
        <a href="https://www.twitch.tv/winzly_" target="_blank" class="twitch"><i class="fab fa-twitch"></i></a>
        <a href="https://dsc.gg/winzly" target="_blank" class="discord"><i class="fab fa-discord"></i></a>
        <a href="https://twitter.com/winzly_" target="_blank" class="twitter"><i class="fab fa-twitter"></i></a>
    </div>

    <script>
        document.getElementById("supportButton").addEventListener("click", function() {
            const centerText = document.getElementById("centerText");
            const message = document.getElementById("copyMessage");

            // Поднятие текста "Winzly's setup"
            centerText.style.top = "10%"; // Двигаем текст вверх

            // Показываем сообщение об успешном копировании
            message.style.display = "block";

            // Через 2 секунды скрываем сообщение
            setTimeout(function() {
                message.style.display = "none";
            }, 2000);

            // Возвращаем текст "Winzly's setup" обратно в исходное положение
            setTimeout(function() {
                centerText.style.top = "35%"; // Возвращаем текст на место
            }, 2500);
        });
    </script>
</body>
</html>
