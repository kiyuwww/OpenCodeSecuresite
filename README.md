<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your IP Address</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: black;
            color: white;
            font-family: Arial, sans-serif;
            font-size: 24px;
        }
        #ip {
            text-align: center;
        }
    </style>
</head>
<body>
    <div id="ip">Fetching your IP address...</div>

    <script>
        fetch('https://api.ipify.org?format=json')
            .then(response => response.json())
            .then(data => {
                document.getElementById('ip').textContent = 'Your IP Address: ' + data.ip;
            })
            .catch(error => {
                document.getElementById('ip').textContent = 'Error fetching IP address';
                console.error('Error:', error);
            });
    </script>
</body>
</html>
