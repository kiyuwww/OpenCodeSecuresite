<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Тёмный сайт</title>
    <style>
        /* Сброс стандартных отступов */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Основные стили для фона и текста */
        body {
            background-color: #0d0d0d; /* Черный фон */
            color: #f0f0f0; /* Светлый текст */
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        /* Контейнер для основного содержимого */
        .container {
            width: 80%;
            max-width: 900px;
            text-align: center;
            padding: 20px;
            background: #1a1a1a; /* Тёмный серый фон контейнера */
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.5); /* Тень */
        }

        /* Стили для заголовка */
        header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        header p {
            font-size: 1.2em;
            color: #b3b3b3;
        }

        /* Основной контент */
        main {
            margin: 20px 0;
        }

        section {
            margin-bottom: 20px;
        }

        h2 {
            font-size: 1.8em;
            color: #e0e0e0;
            margin-bottom: 10px;
        }

        /* Подвал */
        footer {
            margin-top: 20px;
            color: #666666;
            font-size: 0.9em;
        }

        footer p {
            color: #999999;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Добро пожаловать на мой сайт</h1>
            <p>Тёмный дизайн и стиль</p>
        </header>
        <main>
            <section class="content">
                <h2>О нас</h2>
                <p>Здесь можно добавить описание вашей компании или проекта.</p>
            </section>
            <section class="services">
                <h2>Услуги</h2>
                <p>Описание услуг или продуктов, которые вы предлагаете.</p>
            </section>
        </main>
        <footer>
            <p>&copy; 2024 Ваш сайт. Все права защищены.</p>
        </footer>
    </div>
</body>
</html>
