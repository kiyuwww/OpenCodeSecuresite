<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Минималистичный квадратный дизайн</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #0d0d0d; /* Темный фон */
            font-family: 'Arial', sans-serif;
            color: #ffffff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }

        /* Основной контейнер */
        .container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-gap: 20px;
            max-width: 80%;
        }

        /* Квадратные блоки */
        .square {
            width: 100%;
            padding-bottom: 100%; /* Это создает квадрат */
            background-color: #1a1a1a;
            position: relative;
            transition: all 0.3s ease;
            border: 2px solid #333;
        }

        /* Текст внутри квадратов */
        .square p {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            margin: 0;
            font-size: 1.5em;
            letter-spacing: 2px;
            color: #ffffff;
            text-transform: uppercase;
        }

        /* Ховер-эффект */
        .square:hover {
            background-color: #ff6600;
            border-color: #ff6600;
            transform: scale(1.05);
        }

        /* Подвал */
        footer {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            color: #555;
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="square"><p>Home</p></div>
        <div class="square"><p>About</p></div>
        <div class="square"><p>Services</p></div>
        <div class="square"><p>Portfolio</p></div>
        <div class="square"><p>Blog</p></div>
        <div class="square"><p>Contact</p></div>
    </div>

    <footer>
        © 2024 Ваш Сайт. Все права защищены.
    </footer>

</body>
</html>
