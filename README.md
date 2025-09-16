# EX01 Developing a Simple Webserver

# Date:
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```from django.shortcuts import render
from http.server import HTTPServer , BaseHTTPRquestHandler
content ='''<html>
              <h1>**HELLO**</h1>
            </html>'''
class MyServer(BaseHTTPRequestHandler):               
    def do_GET(self):
        print("Get request recived...")
        self.send_respone(200)
        self.send_header("content-type","text/html")
        self.send_header()
        self.wfile.write(content.encode())
 print("this is my webserver")       
 server_address =('',8000)
 httpd = HTTTPServer(server_address,MyServer)
 httpd.server_forever()
 ```

The program for implementing simple webserver is executed successfully.
