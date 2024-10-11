import base64

def encrypt(code):
    return base64.b64encode(code.encode()).decode()

def decrypt(encrypted_code):
    return base64.b64decode(encrypted_code.encode()).decode()

encrypted_code = encrypt("""
from flask import Flask, render_template, request
import requests

app = Flask(__name__)

@app.route('/', methods=['GET', 'POST'])
def index():
    if request.method == 'POST':
        ip_address = request.form['ip_address']
        url = f'https://ipinfo.io/{ip_address}/json'
        response = requests.get(url)
        data = response.json()
        return render_template('index.html', data=data)
    return render_template('index.html')

if __name__ == '__main__':
    app.run()
""")

# Save the encrypted code to a file
with open('encrypted_code.txt', 'w') as file:
    file.write(encrypted_code)
