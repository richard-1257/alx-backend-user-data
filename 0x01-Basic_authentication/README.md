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
+ [x] 0. **Log parsing**<br/>[0-stats.py](0-stats.py): contains a script that reads `stdin` line by line and computes metrics:
  + Input format: `<IP Address> - [<date>] "GET /projects/260 HTTP/1.1" <status code> <file size>` (if the format is not this one, the line must be skipped).
  + After every 10 lines and/or a keyboard interruption `(CTRL + C)`, print these statistics from the beginning:
    + Total file size: `File size: <total size>`.
    + Where `<total size>` is the sum of all previous `<file size>` (see input format above)
    + Number of lines by status code:
      + Possible status code: `200`, `301`, `400`, `401`, `403`, `404`, `405` and `500`.
      + If a status code doesn’t appear or is not an integer, don’t print anything for this status code.
      + Format: `<status code>: <number>`.
      + Status codes should be printed in ascending order. 



