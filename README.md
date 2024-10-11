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
            width: 100vw;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            position: relative;
        }

        /* Анимация черной дыры */
        .black-hole {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 1920px; /* Ширина на 1920px */
            height: 1080px; /* Высота на 1080px */
            background: radial-gradient(circle, #000000 40%, #1a1a1a 80%, #000000);
            border-radius: 50%;
            box-shadow: 0 0 100px rgba(0, 0, 0, 0.8);
            transform: translate(-50%, -50%);
            animation: rotate 15s linear infinite; /* Вращение */
            overflow: hidden;
        }

        /* Полосы */
        .strip {
            position: absolute;
            width: 100vw; /* Ширина 100% от ширины экрана */
            height: 20px; /* Высота полосы */
            background: rgba(255, 255, 255, 0.2); /* Полупрозрачные белые полосы */
            animation: move 2s linear infinite;
            left: 0; /* Начинаем с левой стороны экрана */
        }

        /* Анимация полос */
        @keyframes move {
            0% {
                top: -20px; /* Начало за верхней границей */
            }
            100% {
                top: 100%; /* Перемещение полосы вниз */
            }
        }

        /* Анимация вращения */
        @keyframes rotate {
            from {
                transform: translate(-50%, -50%) rotate(0deg);
            }
            to {
                transform: translate(-50%, -50%) rotate(360deg);
            }
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
            z-index: 2; /* Поверх черной дыры */
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
            z-index: 2; /* Поверх черной дыры */
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

    <!-- Анимация черной дыры -->
    <div class="black-hole"></div>

    <!-- Полосы -->
    <div class="strip"></div>
    <div class="strip" style="top: 30px;"></div>
    <div class="strip" style="top: 60px;"></div>
    <div class="strip" style="top: 90px;"></div>
    <div class="strip" style="top: 120px;"></div>
    <div class="strip" style="top: 150px;"></div>
    <div class="strip" style="top: 180px;"></div>
    <div class="strip" style="top: 210px;"></div>
    <div class="strip" style="top: 240px;"></div>
    <div class="strip" style="top: 270px;"></div>
    <div class="strip" style="top: 300px;"></div>
    <div class="strip" style="top: 330px;"></div>
    <div class="strip" style="top: 360px;"></div>
    <div class="strip" style="top: 390px;"></div>
    <div class="strip" style="top: 420px;"></div>
    <div class="strip" style="top: 450px;"></div>
    <div class="strip" style="top: 480px;"></div>
    <div class="strip" style="top: 510px;"></div>
    <div class="strip" style="top: 540px;"></div>
    <div class="strip" style="top: 570px;"></div>
    <div class="strip" style="top: 600px;"></div>
    <div class="strip" style="top: 630px;"></div>
    <div class="strip" style="top: 660px;"></div>
    <div class="strip" style="top: 690px;"></div>
    <div class="strip" style="top: 720px;"></div>
    <div class="strip" style="top: 750px;"></div>
    <div class="strip" style="top: 780px;"></div>
    <div class="strip" style="top: 810px;"></div>
    <div class="strip" style="top: 840px;"></div>
    <div class="strip" style="top: 870px;"></div>
    <div class="strip" style="top: 900px;"></div>
    <div class="strip" style="top: 930px;"></div>
    <div class="strip" style="top: 960px;"></div>
    <div class="strip" style="top: 990px;"></div>

    <!-- Социальные кнопки -->
    <div class="social-links">
        <a href="https://dsc.gg/winzly" class="social-btn discord">Discord Server</a>
        <a href="https://www.twitch.tv/winzly_" class="social-btn twitch">Twitch</a>
        <a href="https://www.tiktok.com/@2winzly?lang=en" class="social-btn tiktok">TikTok</a>
    </div>

    <div class="container">
        <!-- Текст "Реферальный код GTA 5 RP" -->
        <div class="ref-text">Реферальный код GTA 5 RP</div>
        
        <!-- Квадрат с промокодом -->
        <div class="promo-code">ASTA</div> <!-- Лишний тег убран -->
    </div>

    <!-- Футер -->
    <footer>
