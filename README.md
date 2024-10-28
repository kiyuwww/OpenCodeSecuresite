<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Winzly's Social Networks</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Reset default margins and paddings */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Body styling */
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #121212;
            font-family: Arial, sans-serif;
            color: #fff;
        }

        /* Container styling */
        .container {
            text-align: center;
            padding: 20px;
        }

        /* Social links styling */
        .social-links {
            margin-top: 20px;
        }

        .social-links a {
            color: #fff;
            text-decoration: none;
            font-size: 3rem;
            margin: 0 15px;
            transition: transform 0.3s ease;
        }

        .social-links a:hover {
            transform: scale(1.2);
            color: #00acee; /* You can adjust hover color */
        }

        /* Support button styling */
        .support-button {
            position: absolute;
            top: 20px;
            right: 20px;
            background-color: #1e90ff;
            color: #fff;
            padding: 10px 20px;
            font-size: 1rem;
            font-weight: bold;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            transition: background-color 0.3s;
        }

        .support-button:hover {
            background-color: #0f78d1;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Connect with Winzly</h1>
        <div class="social-links">
            <a href="https://www.twitch.tv/winzly_" target="_blank" aria-label="Twitch"><i class="fab fa-twitch"></i></a>
            <a href="https://dsc.gg/winzly" target="_blank" aria-label="Discord"><i class="fab fa-discord"></i></a>
        </div>
    </div>
    <a href="https://dsc.gg/winzly" target="_blank" class="support-button">Support</a>
</body>
</html>
