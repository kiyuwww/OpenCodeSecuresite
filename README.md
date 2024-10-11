<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Winzly Browser</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #000;
            color: #fff;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .search-container {
            text-align: center;
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

    </style>
</head>
<body>
    <div class="search-container">
        <h1>Winzly Browser</h1>
        <form id="searchForm" action="" method="get" target="_self">
            <input type="text" id="searchInput" placeholder="Введите запрос..." />
            <input type="submit" value="Поиск" />
        </form>
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
