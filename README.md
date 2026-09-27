# SImpleWEBSever
# EX01 Developing a Simple Webserver
## Date:27/9/2026
## AIM:
To develop a simple webserver to serve html pages and display the Device Specifications of your Laptop.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
html_content="""<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>My Simple Server</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .container {
            text-align: center;
            background: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Hello from my server!</h1>
        <p>This page is being served by a simple Python web server.</p>
    </div>
</body>
</html>"""
from http.server import HTTPServer, SimpleHTTPRequestHandler

def run_server(port=8000):
    with open("index.html", "w") as f:
        f.write(html_content)
    server_address = ('', port)
    httpd = HTTPServer(server_address, SimpleHTTPRequestHandler)
    print(f"Serving on http://localhost:{port}")
    httpd.serve_forever()

if __name__ == "__main__":
    run_server()


## OUTPUT:
<img width="1335" height="671" alt="image" src="https://github.com/user-attachments/assets/a46364b0-876d-4969-b688-2061d72f5a9e" />
<img width="1350" height="652" alt="{3F94B4BF-4BC0-4879-B151-8A1C8F3585A8}" src="https://github.com/user-attachments/assets/a89ce403-fb92-44a6-8116-046bb2ac3a8e" />


## RESULT:
The program for implementing simple webserver is executed successfully.
