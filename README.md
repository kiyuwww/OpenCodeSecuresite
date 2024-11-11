<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Winzly Support</title>
  <style>
    body {
      background-color: #000;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }

    .black-hole {
      width: 100px;
      height: 100px;
      background: radial-gradient(circle, rgba(0,0,0,1) 0%, rgba(0,0,0,0) 70%);
      border-radius: 50%;
      position: absolute;
      animation: moveBlackHole 10s linear infinite;
    }

    @keyframes moveBlackHole {
      0% {
        transform: translate(0, 0);
      }
      25% {
        transform: translate(calc(100vw - 100px), 0);
      }
      50% {
        transform: translate(calc(100vw - 100px), calc(100vh - 100px));
      }
      75% {
        transform: translate(0, calc(100vh - 100px));
      }
      100% {
        transform: translate(0, 0);
      }
    }

    .icon-container {
      display: flex;
      gap: 20px;
      padding: 30px;
      border: 2px solid #fff;
      border-radius: 15px;
      transition: all 0.5s ease;
      animation: slideUp 1s ease-in-out;
    }

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

    @keyframes slideUp {
      from { transform: translateY(50px); opacity: 0; }
      to { transform: translateY(0); opacity: 1); }
    }

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

  <div class="support-btn" onclick="copySupport()">Support</div>

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

  <div class="notification" id="copyNotification">Текст скопирован</div>

  <div class="black-hole"></div>

  <script>
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
