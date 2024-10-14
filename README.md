<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Рулетка Плюми</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f5f5f5;
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
            animation: spin 0s ease-in-out;
        }

        .wheel:before {
            content: '';
            width: 4px;
            height: 150px;
            background-color: #333;
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
        }

        .segment:nth-child(1) {
            transform: rotate(45deg);
            background-color: #ffcccb;
        }

        .segment:nth-child(2) {
            transform: rotate(225deg);
            background-color: #add8e6;
        }

        .segment-label {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 20px;
            font-weight: bold;
        }

        button {
            padding: 10px 20px;
            font-size: 16px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:disabled {
            background-color: #cccccc;
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
            <div class="segment" style="transform: rotate(0deg); background-color: #FF6347;">
                <div class="segment-label">Мать Плюми</div>
            </div>
            <div class="segment" style="transform: rotate(180deg); background-color: #4682B4;">
                <div class="segment-label">Батя Плюми</div>
            </div>
        </div>
        <button id="spinButton" onclick="spinWheel()">Spin</button>
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
