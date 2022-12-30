# Developing a Simple Webserver

# AIM:

Develop a webserver to display about top five web application development frameworks.

Name:Thivakar R

Ref.No.:22003745

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
``` from http.server import HTTPServer, BaseHTTPRequestHandler
 
content = """
<html>
</head>
</head>
<body>
<h1>WELCOME</h1>
<h2>NAME: Thivakar R</h2>
<h2>REF.NO.:22003745</h2>
<h3>LIST OF FRAMEWORKS</h3>
<h4>-laravel</h4>
<h4>-meteor</h4>
<h4>-cakePHP</h4>
<h4>-ASP.NET</h4>
<h4>-Laravel</h4>
</body>
</html>
"""
 
class Hellohandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address, Hellohandler)
httpd.serve_forever()
```
# OUTPUT:
![Screenshot (13)](https://user-images.githubusercontent.com/118707074/210051255-457cb219-5d25-4075-9b67-e97734df3c0b.png)

# RESULT:

The program is executed succesfully
