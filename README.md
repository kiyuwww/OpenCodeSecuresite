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
            background-color: #0d0d0d;
            font-family: 'Arial', sans-serif;
            color: #ffffff;
            height: 100vh;
            width: 100vw;
            overflow-x: hidden; /* Убираем горизонтальную прокрутку */
            scroll-behavior: smooth; /* Плавная прокрутка */
        }

        /* Фоновая анимация черной дыры */
        .black-hole {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 1920px;
            height: 1080px;
            background: radial-gradient(circle, #000000 40%, #1a1a1a 80%, #000000);
            border-radius: 50%;
            box-shadow: 0 0 100px rgba(0, 0, 0, 0.8);
            transform: translate(-50%, -50%);
            animation: rotate 15s linear infinite;
            z-index: -1;
        }

        @keyframes rotate {
            from {
                transform: translate(-50%, -50%) rotate(0deg);
            }
            to {
                transform: translate(-50%, -50%) rotate(360deg);
            }
        }

        /* Стили для основного контейнера */
        .container {
            text-align: center;
            width: 100%;
            max-width: 600px;
            position: relative;
            z-index: 1;
            margin: 0 auto;
            padding-top: 150px;
        }

        /* Страница с дополнительным фоном */
        .next-section {
            height: 100vh; /* Высота следующего экрана */
            position: relative;
            background-color: #0d0d0d;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Линии на фоне */
        .strip {
            position: absolute;
            width: 100vw;
            height: 20px;
            background: rgba(255, 255, 255, 0.2);
            animation: move 2s linear infinite;
            left: 0;
        }

        @keyframes move {
            0% {
                top: -20px;
            }
            100% {
                top: 100%;
            }
        }

        /* Контент на первой странице */
        .ref-text {
            font-size: 2em;
            color: #ffffff;
            text-transform: uppercase;
            letter-spacing: 3px;
            margin-bottom: 20px;
        }

        .promo-code {
            font-size: 3em;
            color: #ff6600;
            border: 2px solid #ff6600;
            padding: 20px 50px;
            text-transform: uppercase;
            letter-spacing: 10px;
            display: inline-block;
            background-color: #1a1a1a;
        }

        /* Социальные кнопки */
        .social-links {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 2;
            display: flex;
        }

        .social-btn {
            color: #ffffff;
            font-size: 1.2em;
            text-decoration: none;
            border: 2px solid #ffffff;
            padding: 10px 20px;
            border-radius: 5px;
            margin: 0 15px;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        .social-btn:hover {
            background-color: #ff6600;
            border-color: #ff6600;
        }
    </style>
</head>
<body>
    <!-- Анимация черной дыры -->
    <div class="black-hole"></div>

    <!-- Полосы -->
    <div class="strip"></div>
    <div class="strip" style="top: 30px;"></div>
    <div class="strip" style="top: 60px;"></div>

    <!-- Социальные кнопки -->
    <div class="social-links">
        <a href="https://dsc.gg/winzly" class="social-btn discord">Discord Server</a>
        <a href="https://www.twitch.tv/winzly_" class="social-btn twitch">Twitch</a>
        <a href="https://www.tiktok.com/@2winzly?lang=en" class="social-btn tiktok">TikTok</a>
    </div>

    <!-- Контент первой страницы -->
    <div class="container">
        <div class="ref-text">Реферальный код GTA 5 RP</div>
        <div class="promo-code">ASTA</div>
    </div>

    <!-- Следующая секция (просто фон) -->
    <div class="next-section">
        <div class="black-hole"></div> <!-- Фон черной дыры как на первой странице -->
    </div>

</body>
</html>
