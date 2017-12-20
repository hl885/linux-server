# Linux Server Configuration
This project takes a baseline installation of a Linux server and prepare it to host an web application. The server is secured by enforcing key-based authentication and setting up firewalls to allow few ports.

## Server Info
- The IP address of the server is: 52.14.156.48
- The SSH port accessible is: 2200
- The URL of the hosted web application is: [http://52.14.156.48](http://52.14.156.48)

## Software Installed
The following softwares are installed on the server:
- python3
- python3-pip
- Flask
- SQLAlchemy
- oauth2client
- postgresql
- psycopg2
- apache2
- libapache2-mod-wsgi-py3
- git

## Server Configurations
- All currently installed packages are updated
- The firewall is set up using Uncomplicated Firewall (UFW) to allow only port 2200 (SSH), port 80 (HTTP), and port 123 (ntp)
- The SSH port is changed from port 20 to port 2200
- The root login is disabled
- The key-based authentication is enforced
- The local timezone is set to UTC
- The Apache is configured to serve a Python mod_wsgi application
- A postgresql user named 'catalog' with password 'catalog' is created for the application database 'mycatalog'. The user can only read the database.
- A new user account on server with sudo permission named 'grader' is created. The SSH key is shown in the submission note.

## Third party resource:
- [Apache](https://httpd.apache.org/docs/)
- [Flask mod_wsgi](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/)
