# Echoserver
Echo server and client using python socket
# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
<h2>1.Django</h2>
<h2>2. MEAN Stack</h2>
<h2>3. React </h2>
</body>
</html>


class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('keerthi',2323)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
##  Architecture Diagram

```bash
+--------------------------+
|  User's Web Browser      |
|  (Client: Chrome/Firefox)|
+-----------+--------------+
            |
            |  HTTP Request (GET /)
            v
+-----------+--------------+
|   Python Web Server      |
| (http.server + Handler)  |
| - Listens on Port 8000   |
| - Handles GET Requests   |
| - Sends HTML Response    |
+-----------+--------------+
            |
            |  HTML Response
            v
+--------------------------+
|  User Sees Rendered Page |
|  <h1>Hello Web Server</h1>|
+--------------------------+
```


## OUTPUT:

<img width="1919" height="1143" alt="Screenshot 2026-01-28 091742" src="https://github.com/user-attachments/assets/fc079d64-a544-456a-93f0-76f926892c57" />

### CLIENT OUTPUT:

<img width="592" height="326" alt="Screenshot 2026-01-28 091818" src="https://github.com/user-attachments/assets/510b1875-b942-4d1f-a8bd-497eaa896fb0" />

### SERVER OUTPUT:

<img width="595" height="348" alt="Screenshot 2026-01-28 091810" src="https://github.com/user-attachments/assets/e884f37b-ba7f-4c1b-a6aa-92fdf110b2c0" />

## RESULT:
The program is executed succesfully
