<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Реферальный код GTA 5 RP</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #0d0d0d; /* Черный фон */
            font-family: 'Arial', sans-serif;
            color: #ffffff;
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        /* Стили для кнопок социальных сетей */
        .social-links {
            position: absolute;
            top: 20px;
            left: 50%;
            transform: translateX(-50%); /* Выровняем блок по центру */
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .social-btn {
            color: #ffffff;
            font-size: 1.2em;
            text-decoration: none;
            border: 2px solid #ffffff;
            padding: 10px 20px;
            border-radius: 5px;
            transition: background-color 0.3s ease, color 0.3s ease;
            margin: 0 15px; /* Увеличен отступ между кнопками */
        }

        .social-btn:hover {
            background-color: #ff6600;
            border-color: #ff6600;
            color: #ffffff;
        }

        /* Контейнер для анимации */
        .container {
            text-align: center;
            position: relative;
            width: 100%;
            max-width: 600px;
        }

        /* Текст "Реферальный код GTA 5 RP" */
        .ref-text {
            font-size: 2em;
            color: #ffffff;
            text-transform: uppercase;
            letter-spacing: 3px;
            opacity: 0;
            animation: fadeInText 2s forwards 0.5s;
            margin-bottom: 20px; /* Расстояние до промокода */
        }

        /* Квадрат с промокодом */
        .promo-code {
            font-size: 3em;
            color: #ff6600;
            border: 2px solid #ff6600;
            padding: 20px 50px;
            text-transform: uppercase;
            letter-spacing: 10px;
            display: inline-block;
            background-color: #1a1a1a;
            opacity: 0;
            animation: promoIn 2s forwards 1s;
        }

        /* Анимация для текста "Реферальный код" */
        @keyframes fadeInText {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Анимация для промокода ASTA */
        @keyframes promoIn {
            0% {
                opacity: 0;
                transform: translateY(100%);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Анимация для футера */
        footer {
            position: absolute;
            bottom: 20px;
            color: #555;
            opacity: 0;
            animation: fadeInFooter 2s forwards 2s;
        }

        @keyframes fadeInFooter {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>

    <!-- Социальные кнопки -->
    <div class="social-links">
        <a href="https://dsc.gg/winzly" class="social-btn discord">Discord Server</a>
        <a href="https://www.twitch.tv/winzly_" class="social-btn twitch">Twitch</a>
        <a href="https://www.tiktok.com/@2winzly?lang=en" class="social-btn tiktok">TikTok</a>
    </div>

    <div class="container">
        <!-- Текст "Реферальный код GTA 5 RP" -->
        <div class="ref-text">Реферальный код GTA 5 RP</div>
        
        <!-- Квадрат с промокодом ASTA -->
        <div class="promo-code">ASTA</div>
    </div>

    <footer>
        © 2024 Ваш Сайт. Все права защищены.
    </footer>

</body>
</html>
