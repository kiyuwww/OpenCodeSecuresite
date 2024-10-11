<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Winzly Browser</title>
    <style>
        /* Основные стили для страницы */
        body {
            margin: 0;
            padding: 0;
            background-image: url('https://images.unsplash.com/photo-1506748686214-e9df14d4d9d0'); /* Фон дождливого леса */
            background-size: cover;
            color: #fff;
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }

        /* Стили для контейнера поиска */
        .search-container {
            text-align: center;
            background-color: rgba(0, 0, 0, 0.6); /* Прозрачный фон */
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.7);
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            font-family: 'Courier New', Courier, monospace;
        }

        input[type="text"] {
            padding: 10px;
            width: 300px;
            font-size: 18px;
            border: none;
            border-radius: 5px;
            margin-right: 10px;
        }

        input[type="submit"] {
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            border-radius: 5px;
            background-color: #444;
            color: #fff;
            cursor: pointer;
        }

        input[type="submit"]:hover {
            background-color: #555;
        }

        /* Стили для виджета сверху справа */
        .registration-widget {
            position: absolute;
            top: 20px;
            right: 20px;
            background-color: rgba(0, 0, 0, 0.5);
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 18px;
            font-weight: bold;
        }

        .registration-widget a {
            color: #00aaff;
            text-decoration: none;
        }

        .registration-widget a:hover {
            text-decoration: underline;
        }

        /* Дополнительные виджеты */
        .best-browser-widget {
            position: absolute;
            bottom: 30px;
            left: 30px;
            background-color: rgba(0, 0, 0, 0.6);
            padding: 15px 30px;
            border-radius: 10px;
            font-size: 18px;
            font-family: 'Courier New', Courier, monospace;
        }
    </style>
</head>
<body>
    <!-- Виджет для регистрации -->
    <div class="registration-widget">
        <a href="#">Регистрация</a>
    </div>

    <!-- Основной блок поиска -->
    <div class="search-container">
        <h1>Winzly Browser</h1>
        <form id="searchForm" action="" method="get" target="_self">
            <input type="text" id="searchInput" placeholder="Введите запрос..." />
            <input type="submit" value="Поиск" />
        </form>
    </div>

    <!-- Виджет для информации, что это лучший браузер -->
    <div class="best-browser-widget">
        Лучший браузер для вас: быстрый, удобный, инновационный!
    </div>

    <script>
        document.getElementById("searchForm").onsubmit = function(e) {
            e.preventDefault();
            var query = document.getElementById("searchInput").value;
            if (query) {
                window.location.href = "https://www.google.com/search?q=" + encodeURIComponent(query);
            }
        };
    </script>
</body>
</html>
