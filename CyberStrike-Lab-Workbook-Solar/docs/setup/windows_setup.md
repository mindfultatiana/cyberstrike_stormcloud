# Configure the Windows Machine

### Install the IEEE 2030.5 Server

1. Move the SunSpec IEEE 2030.5 server to the VM into `C:\Copyrighted_Server\DoNotCopyOrStealPlease\`

2. Install [Python 3.9](https://www.python.org/ftp/python/3.9.2/python-3.9.2rc1-amd64.exe)

3. (Optional) Add `C:\Users\Admin\AppData\Local\Programs\Python\Python39\` to the PATH variable. 

4. Create a `run_2030.5_server.bat` with the following `cd C:\Copyrighted_Server\DoNotCopyOrStealPlease\2030_server && C:\Users\Admin\AppData\Local\Programs\Python\Python39\python.exe C:\Copyrighted_Server\DoNotCopyOrStealPlease\2030_server\server.py`

5. Confirm when you run the `.bat` file it opens the port: 

	```
	┌──(kali㉿kali)-[~]
	└─$ nmap 10.10.0.50 -p 9443
	Starting Nmap 7.92 ( https://nmap.org ) at 2022-10-17 18:18 EDT
	Nmap scan report for 10.10.0.50
	Host is up (0.0017s latency).

	PORT     STATE SERVICE
	9443/tcp open  tungsten-https

	Nmap done: 1 IP address (1 host up) scanned in 13.09 seconds
	```
	
#### Flask API
This lab will use Flask API, which is a Python library that allows developers to easily build RESTful APIs using the Flask web framework. It is a lightweight and flexible web framework that provides a minimalistic set of tools for web development, supporting common data formats such as JSON (JavaScript Object Notation) and it can be used with a variety of HTTP (Hypertext Transfer Protocol) clients. 

[Flask](https://flask.palletsprojects.com/en/2.2.x/)

#### Node.js
In this lab we utilize Node.js in order to store the PV data in the DERMS Windows VM. Specifically, it is a server-side runtime environment that allows developers to build scalable, high-performance applications by using an event-driven, non-blocking I/O model that makes it lightweight and efficient. Node.js is built on top of the V8 JavaScript engine from Google, which compiles JavaScript code into machine code at runtime. This allows Node.js to execute JavaScript code on the server, rather than just in the browser. 

[Node.js](https://nodejs.org/en/)