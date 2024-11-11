<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Winzly Support</title>
  <style>
    /* Стили для фона и центрации элементов */
    body {
      background-color: #000;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      font-family: Arial, sans-serif;
    }

    /* Контейнер для иконок */
    .icon-container {
      display: flex;
      gap: 20px;
      padding: 30px;
      border: 2px solid #fff;
      border-radius: 15px;
      transition: all 0.5s ease;
      animation: slideUp 1s ease-in-out;
    }

    /* Иконки и их стили */
    .icon {
      width: 50px;
      height: 50px;
      background-size: cover;
      transition: transform 0.3s, background-color 0.3s;
      cursor: pointer;
      background-color: #fff;
      border-radius: 10px;
    }

    .icon:hover {
      background-color: #000;
      transform: scale(1.1);
    }

    /* Анимация появления иконок снизу */
    @keyframes slideUp {
      from { transform: translateY(50px); opacity: 0; }
      to { transform: translateY(0); opacity: 1); }
    }

    /* Стиль для кнопки Support */
    .support-btn {
      position: absolute;
      top: 20px;
      right: 20px;
      padding: 10px 20px;
      background-color: #555;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .support-btn:hover {
      background-color: #333;
    }

    /* Стиль для уведомления о копировании */
    .notification {
      position: absolute;
      top: 20px;
      background-color: #222;
      color: #fff;
      padding: 10px 20px;
      border-radius: 5px;
      font-size: 14px;
      display: none;
      opacity: 0;
      transition: opacity 0.5s;
    }

    .notification.show {
      display: block;
      opacity: 1;
    }
  </style>
</head>
<body>

  <!-- Кнопка Support -->
  <div class="support-btn" onclick="copySupport()">Support</div>

  <!-- Контейнер для иконок -->
  <div class="icon-container">
    <a href="https://www.twitch.tv/winzly_" target="_blank">
      <div class="icon" style="background-image: url('https://img.icons8.com/ios-filled/50/000000/twitch.png');"></div>
    </a>
    <a href="https://dsc.gg/winzly" target="_blank">
      <div class="icon" style="background-image: url('https://img.icons8.com/ios-filled/50/000000/discord-logo.png');"></div>
    </a>
    <a href="https://twitter.com/2winzly" target="_blank">
      <div class="icon" style="background-image: url('https://img.icons8.com/ios-filled/50/000000/twitter.png');"></div>
    </a>
  </div>

  <!-- Уведомление о копировании -->
  <div class="notification" id="copyNotification">Текст скопирован</div>

  <script>
    // Функция копирования текста
    function copySupport() {
      navigator.clipboard.writeText('.winzly');
      const notification = document.getElementById('copyNotification');
      notification.classList.add('show');
      setTimeout(() => {
        notification.classList.remove('show');
      }, 2000);
    }
  </script>

</body>
</html>
