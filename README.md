<!DOCTYPE html>
<html>
<head>
    <title>IP Info</title>
</head>
<body>
    <h1>IP Info</h1>
    <form method="POST">
        <input type="text" name="ip_address" placeholder="Enter IP address">
        <button type="submit">Submit</button>
    </form>
    {% if data %}
        <h2>IP Data</h2>
        <ul>
            {% for key, value in data.items() %}
                <li>{{ key }}: {{ value }}</li>
            {% endfor %}
        </ul>
    {% endif %}
</body>
</html>
