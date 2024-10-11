<html>
<head>
    <title>IP Info</title>
    <style>
        body {
            background-color: black;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>IP Info</h1>
        <p id="ip-data"></p>
    </div>

    <script>
        // Encryption and decryption functions
        function encrypt(code) {
            // Implement your encryption algorithm here
            // For example, you can use a simple XOR cipher
            let encrypted = '';
            for (let i = 0; i < code.length; i++) {
                encrypted += String.fromCharCode(code.charCodeAt(i) ^ 42);
            }
            return encrypted;
        }

        function decrypt(encrypted_code) {
            // Implement your decryption algorithm here
            // For example, you can use the same XOR cipher used for encryption
            let decrypted = '';
            for (let i = 0; i < encrypted_code.length; i++) {
                decrypted += String.fromCharCode(encrypted_code.charCodeAt(i) ^ 42);
            }
            return decrypted;
        }

        // Fetch IP data from the ipinfo.io API
        async function fetchIPData() {
            const encrypted_url = '<encrypted_url>';
            const encrypted_api_key = '<encrypted_api_key>';

            const url = decrypt(encrypted_url);
            const api_key = decrypt(encrypted_api_key);

            const response = await fetch(`${url}?token=${api_key}`);
            const data = await response.json();

            return data;
        }

        // Display IP data on the page
        async function displayIPData() {
            const ip_data = await fetchIPData();
            const ip_data_element = document.getElementById('ip-data');

            let data_string = '';
            for (const [key, value] of Object.entries(ip_data)) {
                data_string += `${key}: ${value}\n`;
            }

            ip_data_element.textContent = data_string;
        }

        displayIPData();
    </script>
</body>
</html>
