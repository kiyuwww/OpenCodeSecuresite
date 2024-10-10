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
        }

        /* Контейнер для анимации */
        .container {
            text-align: center;
            position: relative;
            width: 100%;
            height: 100%;
        }

        /* Текст "Реферальный код GTA 5 RP" */
        .ref-text {
            font-size: 2em;
            color: #ffffff;
            text-transform: uppercase;
            letter-spacing: 3px;
            opacity: 0;
            animation: fadeInText 2s forwards 0.5s;
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
            position: absolute;
            background-color: #1a1a1a;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
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
                transform: translate(-50%, -200%);
            }
            50% {
                opacity: 0.5;
                transform: translate(-50%, 50%);
            }
            100% {
                opacity: 1;
                transform: translate(-50%, -50%);
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
