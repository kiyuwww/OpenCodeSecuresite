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
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        /* Общий фон для секций */
        .section {
            height: 100vh; /* Высота секции на весь экран */
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
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

        /* Анимация вращения черной дыры */
        @keyframes rotate {
            from {
                transform: translate(-50%, -50%) rotate(0deg);
            }
            to {
                transform: translate(-50%, -50%) rotate(360deg);
            }
        }

        /* Полосы */
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

        /* Контейнер с контентом на первой странице */
        .container {
            text-align: center;
            z-index: 1;
        }

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
    <!-- Первая секция -->
    <div class="section">
        <div class="black-hole"></div>
        <div class="strip"></div>
        <div class="strip" style="top: 30px;"></div>
        <div class="strip" style="top: 60px;"></div>
        <div class="strip" style="top: 90px;"></div>
        <div class="strip" style="top: 120px;"></div>
        <div class="container">
            <div class="ref-text">Реферальный код GTA 5 RP</div>
            <div class="promo-code">ASTA</div>
        </div>
    </div>

    <!-- Вторая секция (повторение анимации) -->
    <div class="section">
        <div class="black-hole"></div>
        <div class="strip"></div>
        <div class="strip" style="top: 30px;"></div>
        <div class="strip" style="top: 60px;"></div>
        <div class="strip" style="top: 90px;"></div>
        <div class="strip" style="top: 120px;"></div>
    </div>

    <!-- Третья секция (еще одно повторение) -->
    <div class="section">
        <div class="black-hole"></div>
        <div class="strip"></div>
        <div class="strip" style="top: 30px;"></div>
        <div class="strip" style="top: 60px;"></div>
        <div class="strip" style="top: 90px;"></div>
        <div class="strip" style="top: 120px;"></div>
    </div>

    <!-- Социальные кнопки остаются фиксированными -->
    <div class="social-links">
        <a href="https://dsc.gg/winzly" class="social-btn discord">Discord Server</a>
        <a href="https://www.twitch.tv/winzly_" class="social-btn twitch">Twitch</a>
        <a href="https://www.tiktok.com/@2winzly?lang=en" class="social-btn tiktok">TikTok</a>
    </div>
</body>
</html>
