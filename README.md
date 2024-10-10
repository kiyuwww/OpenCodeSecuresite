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
            background-color: #0d0d0d; /* Темный фон */
            font-family: 'Arial', sans-serif;
            color: #ffffff;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        /* Превью контейнер */
        .preview {
            text-align: center;
            background-color: #1a1a1a;
            border: 2px solid #ff6600;
            border-radius: 10px;
            padding: 40px;
            width: 80%;
            max-width: 600px;
        }

        /* Заголовок */
        .preview h1 {
            font-size: 3em;
            letter-spacing: 3px;
            color: #ff6600; /* Оранжевый акцент */
            margin: 0 0 20px;
        }

        /* Текстовый блок */
        .preview p {
            font-size: 1.2em;
            color: #cccccc;
            margin-bottom: 30px;
        }

        /* Реферальный код */
        .ref-code {
            display: inline-block;
            background-color: #333;
            color: #ff6600;
            padding: 15px 40px;
            font-size: 2em;
            border-radius: 5px;
            letter-spacing: 5px;
            border: 2px solid #ff6600;
            transition: all 0.3s ease;
        }

        /* Эффект при наведении на реферальный код */
        .ref-code:hover {
            background-color: #ff6600;
            color: #ffffff;
        }

        /* Кнопка скопировать */
        .copy-btn {
            margin-top: 20px;
            padding: 10px 20px;
            font-size: 1.2em;
            background-color: #ff6600;
            color: #ffffff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .copy-btn:hover {
            background-color: #e65c00;
        }

        /* Подвал */
        footer {
            position: absolute;
            bottom: 20px;
            color: #555;
        }
    </style>
</head>
<body>

    <div class="preview">
        <h1>GTA 5 RP</h1>
        <p>Используйте реферальный код ниже, чтобы получить бонусы и преимущества!</p>
        <div class="ref-code">ASTA</div>
        <button class="copy-btn" onclick="copyCode()">Скопировать код</button>
    </div>

    <footer>
        © 2024 Ваш Сайт. Все права защищены.
    </footer>

    <script>
        function copyCode() {
            const code = document.querySelector('.ref-code').textContent;
            navigator.clipboard.writeText(code).then(() => {
                alert('Реферальный код скопирован: ' + code);
            });
        }
    </script>

</body>
</html>
