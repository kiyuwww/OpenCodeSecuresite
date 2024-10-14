<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Рулетка Плюми</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: #1c1c1c;
            color: white;
        }

        .wheel-container {
            text-align: center;
        }

        .wheel {
            width: 300px;
            height: 300px;
            border: 5px solid #333;
            border-radius: 50%;
            position: relative;
            margin-bottom: 20px;
            box-shadow: 0 0 15px rgba(255, 255, 255, 0.1);
            background: radial-gradient(circle, #2d2d2d 50%, #1c1c1c);
        }

        .wheel:before {
            content: '';
            width: 4px;
            height: 150px;
            background-color: #ffbf00;
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
        }

        .segment {
            width: 150px;
            height: 150px;
            position: absolute;
            top: 0;
            left: 50%;
            transform-origin: 0 100%;
            border-radius: 50%;
            box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.5);
        }

        .segment:nth-child(1) {
            transform: rotate(45deg);
            background: linear-gradient(45deg, #ff6363, #ff3333);
        }

        .segment:nth-child(2) {
            transform: rotate(225deg);
            background: linear-gradient(45deg, #1e90ff, #0077ff);
        }

        .segment-label {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 22px;
            font-weight: bold;
            color: white;
            text-shadow: 0 0 5px rgba(0, 0, 0, 0.7);
        }

        button {
            padding: 12px 30px;
            font-size: 18px;
            font-weight: bold;
            background-color: #ffbf00;
            color: #1c1c1c;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: background-color 0.3s;
            box-shadow: 0 0 15px rgba(255, 191, 0, 0.5);
        }

        button:hover {
            background-color: #ffa500;
        }

        button:disabled {
            background-color: #4d4d4d;
            cursor: not-allowed;
        }

        #result {
            font-size: 24px;
            margin-top: 20px;
            font-weight: bold;
        }

        @keyframes spin {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }
    </style>
</head>
<body>

    <div class="wheel-container">
        <div id="wheel" class="wheel">
            <div class="segment" style="transform: rotate(0deg);">
                <div class="segment-label">Мать Плюми</div>
            </div>
            <div class="segment" style="transform: rotate(180deg);">
                <div class="segment-label">Батя Плюми</div>
            </div>
        </div>
        <button id="spinButton" onclick="spinWheel()">SPIN</button>
        <p id="result"></p>
    </div>

    <script>
        function spinWheel() {
            const wheel = document.getElementById('wheel');
            const button = document.getElementById('spinButton');
            const result = document.getElementById('result');
            const segments = ["Мать Плюми", "Батя Плюми"];
            
            // Отключаем кнопку, пока крутится колесо
            button.disabled = true;
            result.textContent = "";

            const randomDeg = Math.floor(Math.random() * 3600) + 360; // Случайное количество градусов
            wheel.style.transition = 'transform 4s ease-out';
            wheel.style.transform = `rotate(${randomDeg}deg)`;

            setTimeout(() => {
                // Определяем результат
                const selectedSegment = randomDeg % 360 < 180 ? segments[0] : segments[1];
                result.textContent = `Вы выбили: ${selectedSegment}`;

                // Возвращаем кнопку в активное состояние
                button.disabled = false;
            }, 4000);
        }
    </script>

</body>
</html>
