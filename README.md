<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Winzly's Gaming Setup</title>
    <style>
        body {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #1e1e1e;
            color: white;
            font-family: Arial, sans-serif;
            overflow: hidden;
        }
        .container {
            text-align: center;
            position: relative;
            z-index: 10;
        }
        h1 {
            font-size: 2em;
            margin-bottom: 0.2em;
        }
        p {
            font-size: 1em;
            margin-bottom: 1em;
            color: #cccccc;
        }
        .social-links {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin-bottom: 1.5em;
        }
        .social-links a {
            text-decoration: none;
            color: white;
            padding: 8px 15px;
            border-radius: 5px;
            background-color: #333;
            display: flex;
            align-items: center;
            font-size: 1em;
            transition: background-color 0.3s;
        }
        .social-links a:hover {
            background-color: #555;
        }
        .toggle-theme {
            position: absolute;
            top: 20px;
            right: 20px;
            background-color: #333;
            color: white;
            padding: 5px 10px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            font-size: 0.9em;
        }
        .site-link {
            margin-top: 1em;
            font-size: 0.9em;
            color: #777;
        }
        /* Черная дыра */
        .black-hole {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 200px;
            height: 200px;
            margin-top: -100px;
            margin-left: -100px;
            border-radius: 50%;
            background: conic-gradient(from 0deg, #000, #333, #000, #111);
            animation: spin 5s linear infinite;
            z-index: 1;
            filter: blur(2px);
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <button class="toggle-theme">Toggle Theme</button>
    <div class="container">
        <h1>Welcome to Winzly's Gaming Setup</h1>
        <p>Explore my gaming settings and connect with me on social media!</p>
        <div class="social-links">
            <a href="https://www.twitch.tv/winzly_">Twitch</a>
            <a href="https://www.youtube.com">YouTube</a>
            <a href="https://dsc.gg/winzly">Discord</a>
            <a href="https://store.steampowered.com">Steam</a>
        </div>
        <div class="site-link">winzlysite.io</div>
    </div>
    <div class="black-hole"></div>
</body>
</html>
