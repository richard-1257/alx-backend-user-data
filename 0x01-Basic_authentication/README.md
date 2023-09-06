![auth](https://github.com/richard-1257/alx-backend-user-data/assets/83041703/7b54389e-c66d-47a9-9500-9f5e519a9ef5)

# Basic authentication
**Background Context**
In this project, you will learn what the authentication process means and implement a Basic Authentication on a simple API. `Back-end`
`Authentification`

In the industry, you should not implement your own Basic authentication system and use a module or framework that doing it for you (like in Python-Flask: [Flask-HTTPAuth](https://flask-httpauth.readthedocs.io/en/latest/)). Here, for the learning purpose, we will walk through each step of this mechanism to understand it by doing.

## Resources
- [REST API Authentication Mechanisms](https://www.youtube.com/watch?v=501dpx2IjGY)
- [Base64 in Python](https://docs.python.org/3.7/library/base64.html)
- [HTTP header Authorization](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization)
- [Flask](https://palletsprojects.com/p/flask/)
- [Base64 - concep](https://en.wikipedia.org/wiki/Base64)

## Learning Objectives
- What authentication means
- What Base64 is
- How to encode a string in Base64
- What Basic authentication means
- How to send the Authorization header

## Tasks To Complete
+ [x] 0. **Simple-basic-API**<br/>
  + Setup and start server:
```python
bob@dylan:~$ pip3 install -r requirements.txt
...
bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
 * Serving Flask app "app" (lazy loading)
...
bob@dylan:~$
``` 
  + Use the API (in another tab or in your browser):
```python
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/status" -vvv
*   Trying 0.0.0.0...
* TCP_NODELAY set
* Connected to 0.0.0.0 (127.0.0.1) port 5000 (#0)
> GET /api/v1/status HTTP/1.1
> Host: 0.0.0.0:5000
> User-Agent: curl/7.54.0
> Accept: */*
>
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Content-Type: application/json
< Content-Length: 16
< Access-Control-Allow-Origin: *
< Server: Werkzeug/1.0.1 Python/3.7.5
< Date: Mon, 18 May 2020 20:29:21 GMT
<
{"status":"OK"}
* Closing connection 0
bob@dylan:~$
```




