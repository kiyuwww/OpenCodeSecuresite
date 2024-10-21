<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Последние новости и результаты гонок Формулы 1">
    <title>Формула 1 - Гонки и Результаты</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #0f0f0f;
            color: #fff;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #1c1c1c;
            color: #ff4141;
            padding: 20px;
            text-align: center;
            position: sticky;
            top: 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }
        nav {
            display: flex;
            justify-content: center;
            margin: 20px 0;
        }
        nav a {
            margin: 0 15px;
            text-decoration: none;
            color: #ff4141;
            font-weight: bold;
            padding: 10px 20px;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        nav a:hover {
            background-color: #ff4141;
            color: #fff;
        }
        section {
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        h2 {
            color: #ff4141;
            text-align: center;
            margin-bottom: 40px;
            text-transform: uppercase;
        }
        .race-card {
            background-color: #1c1c1c;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(255, 65, 65, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .race-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 20px rgba(255, 65, 65, 0.3);
        }
        .race-card h3 {
            margin: 0;
            color: #ff4141;
        }
        .race-card p {
            margin: 10px 0;
        }
        footer {
            background-color: #1c1c1c;
            color: #ff4141;
            text-align: center;
            padding: 20px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>

    <header>
        <h1>Формула 1 - Гонки и Результаты</h1>
    </header>

    <nav>
        <a href="#">Главная</a>
        <a href="#">Календарь гонок</a>
        <a href="#">Результаты</a>
        <a href="#">Команды и Пилоты</a>
        <a href="#">Новости</a>
    </nav>

    <section>
        <h2>Предстоящие гонки</h2>
        <div class="race-card">
            <h3>Гран-при США</h3>
            <p>Дата: 22 октября 2024</p>
            <p>Место: Трасса в Остине, Техас</p>
        </div>
        <div class="race-card">
            <h3>Гран-при Мексики</h3>
            <p>Дата: 29 октября 2024</p>
            <p>Место: Автодром имени братьев Родригес, Мехико</p>
        </div>
    </section>

    <footer>
        <p>© 2024 Формула 1. Все права защищены.</p>
    </footer>

</body>
</html>
