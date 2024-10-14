<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Продажа квартир в вашем городе. Выберите жилье своей мечты!">
    <title>Продажа Квартир</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f9fa;
        }
        header {
            background-color: #007bff;
            color: white;
            padding: 15px 0;
            text-align: center;
        }
        header h1 {
            margin: 0;
        }
        nav {
            display: flex;
            justify-content: space-around;
            background-color: #343a40;
            padding: 10px 0;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 10px;
        }
        nav a:hover {
            background-color: #007bff;
        }
        .hero {
            text-align: center;
            padding: 50px;
            background: url('your-image-url.jpg') no-repeat center center/cover;
            color: white;
        }
        .hero h2 {
            font-size: 3em;
        }
        .filter {
            padding: 20px;
            background-color: #e9ecef;
            text-align: center;
        }
        .filter input, .filter select {
            padding: 10px;
            margin: 10px;
            width: 200px;
        }
        .apartment-list {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            padding: 20px;
        }
        .apartment {
            background-color: white;
            width: 30%;
            margin: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .apartment img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        .apartment-info {
            padding: 15px;
        }
        .apartment-info h3 {
            margin: 0;
        }
        .apartment-info p {
            color: #6c757d;
        }
        footer {
            background-color: #343a40;
            color: white;
            text-align: center;
            padding: 20px;
        }
        footer a {
            color: #007bff;
            text-decoration: none;
        }
        footer a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <header>
        <h1>Продажа Квартир</h1>
    </header>

    <nav>
        <a href="#">Главная</a>
        <a href="#">Каталог квартир</a>
        <a href="#">О компании</a>
        <a href="#">Контакты</a>
    </nav>

    <section class="hero">
        <h2>Найдите квартиру своей мечты</h2>
        <p>Лучшие предложения на рынке недвижимости</p>
    </section>

    <section class="filter">
        <h3>Фильтр поиска</h3>
        <input type="text" placeholder="Город">
        <input type="number" placeholder="Цена от">
        <input type="number" placeholder="Цена до">
        <select>
            <option value="">Количество комнат</option>
            <option value="1">1 комната</option>
            <option value="2">2 комнаты</option>
            <option value="3">3 комнаты</option>
        </select>
        <button>Поиск</button>
    </section>

    <section class="apartment-list">
        <div class="apartment">
            <img src="apartment1.jpg" alt="Квартира 1">
            <div class="apartment-info">
                <h3>Квартира в центре</h3>
                <p>Цена: 5,000,000 ₽</p>
                <p>3 комнаты, 120 м²</p>
            </div>
        </div>

        <div class="apartment">
            <img src="apartment2.jpg" alt="Квартира 2">
            <div class="apartment-info">
                <h3>Квартира у парка</h3>
                <p>Цена: 3,500,000 ₽</p>
                <p>2 комнаты, 85 м²</p>
            </div>
        </div>

        <div class="apartment">
            <img src="apartment3.jpg" alt="Квартира 3">
            <div class="apartment-info">
                <h3>Элитная квартира</h3>
                <p>Цена: 12,000,000 ₽</p>
                <p>4 комнаты, 200 м²</p>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 Продажа Квартир. Все права защищены.</p>
        <p><a href="mailto:info@example.com">Свяжитесь с нами</a></p>
    </footer>

</body>
</html>
