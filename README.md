<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animated Black Hole</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: black;
            overflow: hidden;
        }

        /* Анимация черной дыры */
        @keyframes spin {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }

        .black-hole {
            position: absolute;
            width: 100vw;
            height: 100vh;
            background: radial-gradient(circle, black 20%, transparent 70%);
            animation: spin 10s linear infinite;
            z-index: -1;
        }

        .stripes {
            position: absolute;
            width: 100vw;
            height: 100vh;
            background: repeating-conic-gradient(
                from 0deg,
                white 0deg 10deg,
                transparent 10deg 20deg
            );
            animation: spin 5s linear infinite reverse;
            z-index: -2;
        }

        /* Виджет */
        .widget {
            text-align: center;
            border: 2px solid red;
            padding: 20px;
            color: white;
            font-family: Arial, sans-serif;
            background-color: rgba(0, 0, 0, 0.7);
            width: 300px;
            border-radius: 15px;
        }

        .widget h1 {
            color: red;
            font-size: 24px;
            margin-bottom: 10px;
        }

        .widget p {
            font-size: 18px;
            margin: 0;
        }

        /* Анимация соединения виджета */
        @keyframes pulse {
            0% {
                box-shadow: 0 0 10px rgba(255, 0, 0, 0.5);
            }
            100% {
                box-shadow: 0 0 30px rgba(255, 0, 0, 1);
            }
        }

        .widget {
            animation: pulse 1.5s infinite alternate;
        }
    </style>
</head>
<body>
    <!-- Черная дыра -->
    <div class="black-hole"></div>
    <div class="stripes"></div>

    <!-- Виджет -->
    <div class="widget">
        <h1>My Discord</h1>
        <p>.winzly</p>
    </div>
</body>
</html>
