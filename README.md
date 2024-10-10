<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Черный сайт</title>
    <style>
        /* Общие стили */
        body {
            margin: 0;
            padding: 0;
            background-color: #000000;
            color: #ffffff;
            font-family: Arial, sans-serif;
        }

        /* Контейнер для содержимого */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Заголовок */
        h1 {
            text-align: center;
            font-size: 3em;
            margin-top: 50px;
        }

        /* Кнопка */
        .btn {
            display: inline-block;
            background-color: #ffffff;
            color: #000000;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            font-size: 1.2em;
            transition: background-color 0.3s ease;
        }

        .btn:hover {
            background-color: #ff6600;
            color: #ffffff;
        }

        /* Подвал */
        footer {
            text-align: center;
            padding: 20px;
            background-color: #1a1a1a;
            position: absolute;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Добро пожаловать на черный сайт</h1>
        <p style="text-align: center;">Это простой пример сайта с черным дизайном. Нажмите на кнопку ниже, чтобы узнать больше.</p>
        <div style="text-align: center;">
            <a href="#" class="btn">Подробнее</a>
        </div>
    </div>

    <footer>
        <p>© 2024 Ваш Сайт. Все права защищены.</p>
    </footer>
</body>
</html>
