<!DOCTYPE html>
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
      animation: fadeIn 1s ease-in-out;
    }

    /* Иконки и их анимация */
    .icon {
      width: 50px;
      height: 50px;
      background-size: cover;
      transition: 0.3s;
      cursor: pointer;
      filter: grayscale(1);
    }

    .icon:hover {
      filter: grayscale(0);
      background-color: #000;
      border-radius: 10px;
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

    /* Анимация появления иконок */
    @keyframes fadeIn {
      from { transform: scale(0.8); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
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
      <div class="icon" style="background-image: url('https://img.icons8.com/ios-filled/50/ffffff/twitch.png');"></div>
    </a>
    <a href="https://dsc.gg/winzly" target="_blank">
      <div class="icon" style="background-image: url('https://img.icons8.com/ios-filled/50/ffffff/discord-logo.png');"></div>
    </a>
    <a href="https://twitter.com/2winzly" target="_blank">
      <div class="icon" style="background-image: url('https://img.icons8.com/ios-filled/50/ffffff/twitter.png');"></div>
    </a>
  </div>

  <!-- Уведомление о копировании -->
  <div class="notification" id="copyNotification">Текст скопирован: .winzly</div>

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
