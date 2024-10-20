<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OpenSourceBrowser</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="browser">
        <div class="browser-header">
            <input type="text" id="url-bar" placeholder="Enter URL...">
            <button id="go-btn">Go</button>
        </div>
        <iframe id="browser-frame" src="https://www.mozilla.org" frameborder="0"></iframe>
    </div>

    <script src="main.js"></script>
</body>
</html>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    background-color: #f5f5f5;
}

.browser {
    display: flex;
    flex-direction: column;
    height: 100vh;
}

.browser-header {
    display: flex;
    justify-content: space-between;
    background-color: #282c34;
    padding: 10px;
}

#url-bar {
    flex: 1;
    padding: 8px;
    font-size: 16px;
    border: none;
    outline: none;
    color: #282c34;
    border-radius: 4px;
}

#go-btn {
    padding: 8px 16px;
    margin-left: 10px;
    background-color: #61dafb;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

#browser-frame {
    flex: 1;
    width: 100%;
    border: none;
}
document.getElementById('go-btn').addEventListener('click', function() {
    const urlBar = document.getElementById('url-bar');
    const browserFrame = document.getElementById('browser-frame');
    const url = urlBar.value.startsWith('http') ? urlBar.value : `https://${urlBar.value}`;
    browserFrame.src = url;
});
