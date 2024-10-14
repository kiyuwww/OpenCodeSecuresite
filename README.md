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
            position: relative;
        }

        .wheel {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            border: 8px solid #333;
            box-shadow: 0 0 15px rgba(255, 255, 255, 0.2);
            background: conic-gradient(
                #ff6363 0 50%, 
                #1e90ff 50% 100%
            );
            position: relative;
            transition: transform 4s ease-out;
        }

        .segment-label {
            position: absolute;
            top: 50%;
            left: 50%;
            font-size: 22px;
            font-weight: bold;
            text-shadow: 0 0 5px rgba(0, 0, 0, 0.7);
            color: white;
        }

        .mother {
            transform: translate(-100%, -150%) rotate(-90deg);
        }

        .father {
            transform: translate(50%, -50%) rotate(90deg);
        }

        /* Добавляем стрелку */
        .arrow {
            width: 0; 
            height: 0; 
            border-left: 20px solid transparent;
            border-right: 20px solid transparent;
            border-bottom: 30px solid #ffbf00;
            position: absolute;
            top: -40px;
            left: 50%;
            transform: translateX(-50%);
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
            margin-top: 20px;
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
    </style>
</head>
<body>

    <div class="wheel-container">
        <div class="arrow"></div>
        <div id="wheel" class="wheel">
            <div class="segment-label mother">Мать Плюми</div>
            <div class="segment-label father">Батя Плюми</div>
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
