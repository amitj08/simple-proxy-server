# Proxy Server
A multithreaded proxy server in python, implemented using threading and sockets as a part of Computer Networks coursework. As of now it supports HTTP websites only.

### Features
- Multi Threaded : can handle multiple clients and server 
- Multiple Clients can be routed through this server.
- Caching : Websites are cached in case of frequent requests (more than 3 times) within a period of 5 minutes.
- Blackilisting: Blocking of websites using a CIDR list (stored in `proxy/blacklist.txt`)
- Authentication : username and password required to view blacklisted domains(stored in `proxy/authentication.txt`)
- Tested on following http websites:
    - [Baidu](www.baidu.com)
    - [ICZN](www.iczn.org)

### To Run
- Fix the port on your host to 20100 (server assumes to be on the port 20100 and re-routes requests through it).
```sh
python server.py
```
- Now we are ready to open a http website on the web browser after fixing the port as described earlier.