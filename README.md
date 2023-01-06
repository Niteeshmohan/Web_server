# Developing a Simple Webserver

# AIM:

name : Niteesh M
ref no : 22008756

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
``` 
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
</head>
</head>
<body>
<h1>WELCOME</h1>
<h2>NAME:G CHETHAN KUMAR</h2>
<h2>REF.NO.:22005596</h2>
<h3>LIST OF FRAMEWORKS</h3>
<h4>-Django</h4>
<h4>-Ruby on Rails</h4>
<h4>-Angular</h4>
<h4>-Meteor</h4>
<h4>-jQuery</h4>
</body>
</html>
"""

class Hellohandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address, Hellohandler)
httpd.serve_forever()
```

# OUTPUT:
![image](https://user-images.githubusercontent.com/119575445/210960296-311ad494-ecb5-40d6-a8b0-ee3a1ebc7e39.png)

# RESULT:

The program is executed succesfully
