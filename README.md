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
            background-image: url('https://images.unsplash.com/photo-1506748686214-e9df14d4d9d0');
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
            background-color: rgba(0, 0, 0, 0.6);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.7);
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            font-family: 'Courier New', Courier, monospace;
        }

        input[type="text"], input[type="password"] {
            padding: 10px;
            width: 300px;
            font-size: 18px;
            border: none;
            border-radius: 5px;
            margin-right: 10px;
            margin-bottom: 10px;
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

        /* Модальное окно для регистрации/входа */
        .modal {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: rgba(0, 0, 0, 0.9);
            padding: 30px;
            border-radius: 10px;
            z-index: 10;
            text-align: center;
        }

        .modal.active {
            display: block;
        }

        .close-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            color: #fff;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <!-- Виджет для регистрации -->
    <div class="registration-widget">
        <a href="#" id="openModal">Регистрация / Вход</a>
    </div>

    <!-- Модальное окно для регистрации/входа -->
    <div id="authModal" class="modal">
        <span class="close-btn" id="closeModal">&times;</span>
        <h2>Регистрация / Вход</h2>
        <form id="authForm">
            <input type="text" id="emailInput" placeholder="Введите email" required><br>
            <input type="password" id="passwordInput" placeholder="Введите пароль" required><br>
            <input type="submit" value="Зарегистрироваться / Войти">
        </form>
        <p id="message" style="color: red; display: none;"></p>
    </div>

    <!-- Основной блок поиска -->
    <div class="search-container" id="searchContainer" style="display: none;">
        <h1>Winzly Browser</h1>
        <form id="searchForm" action="" method="get" target="_self">
            <input type="text" id="searchInput" placeholder="Введите запрос..." />
            <input type="submit" value="Поиск" />
        </form>
    </div>

    <script>
        // Открыть/закрыть модальное окно
        const openModalBtn = document.getElementById('openModal');
        const closeModalBtn = document.getElementById('closeModal');
        const modal = document.getElementById('authModal');
        const searchContainer = document.getElementById('searchContainer');
        const message = document.getElementById('message');

        openModalBtn.onclick = () => {
            modal.classList.add('active');
        }

        closeModalBtn.onclick = () => {
            modal.classList.remove('active');
        }

        // Функция регистрации / входа
        document.getElementById('authForm').onsubmit = function(e) {
            e.preventDefault();
            const email = document.getElementById('emailInput').value;
            const password = document.getElementById('passwordInput').value;

            // Проверяем, есть ли пользователь в LocalStorage
            const storedPassword = localStorage.getItem(email);

            if (storedPassword) {
                // Если пользователь существует, проверяем пароль
                if (storedPassword === password) {
                    alert('Успешный вход!');
                    modal.classList.remove('active');
                    searchContainer.style.display = 'block';
                } else {
                    message.textContent = 'Неверный пароль!';
                    message.style.display = 'block';
                }
            } else {
                // Если пользователя нет, регистрируем его
                localStorage.setItem(email, password);
                alert('Успешная регистрация!');
                modal.classList.remove('active');
                searchContainer.style.display = 'block';
            }
        }

        // Функция поиска
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
