<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Анимированный Сайт</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ff7e5f, #feb47b);
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .container {
            text-align: center;
            color: #fff;
        }

        h1 {
            font-size: 3em;
            letter-spacing: 4px;
            margin-bottom: 20px;
            opacity: 0;
            animation: fadeIn 3s ease-in-out forwards, moveText 6s ease-in-out infinite alternate;
        }

        @keyframes fadeIn {
            0% {
                opacity: 0;
                transform: translateY(50px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes moveText {
            0% {
                letter-spacing: 4px;
                text-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            }
            100% {
                letter-spacing: 10px;
                text-shadow: 0 0 30px rgba(0, 0, 0, 0.8);
            }
        }

        p {
            font-size: 1.5em;
            opacity: 0;
            animation: fadeInText 4s ease-in-out 1s forwards;
        }

        @keyframes fadeInText {
            0% {
                opacity: 0;
                transform: translateY(30px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .button {
            display: inline-block;
            padding: 15px 30px;
            margin-top: 30px;
            font-size: 1.2em;
            color: #fff;
            background-color: rgba(0, 0, 0, 0.3);
            border: none;
            border-radius: 30px;
            cursor: pointer;
            text-decoration: none;
            transition: background-color 0.4s ease;
        }

        .button:hover {
            background-color: rgba(0, 0, 0, 0.6);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Добро пожаловать!</h1>
        <p>Это пример красивого анимированного сайта с эффектом плавного появления текста и кнопки.</p>
        <a href="#" class="button">Нажми на меня</a>
    </div>
</body>
</html>
