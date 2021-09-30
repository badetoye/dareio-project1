## WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS

### What is a Technology stack?
A technology stack is a set of frameworks and tools used to develop a software product. This set of frameworks and tools are very specifically chosen to work together in creating a well-functioning software. They are acronymns for individual technologies used together for a specific technology product. some examples are…

- LAMP (Linux, Apache, MySQL, PHP or Python, or Perl)
- LEMP (Linux, Nginx, MySQL, PHP or Python, or Perl)
- MERN (MongoDB, ExpressJS, ReactJS, NodeJS)
- MEAN (MongoDB, ExpressJS, AngularJS, NodeJS

### Spin up an EC2 instance and allow port 22 (for SSH) and port 80 (for HTTP) ingress access from anywhere
<img width="745" alt="Instance-shot" src="https://user-images.githubusercontent.com/40571508/135457594-8972241d-73b4-4894-ae57-97649b0e6910.PNG">

STEP 1 — INSTALLING APACHE AND UPDATING THE FIREWALL

**Apache HTTP Server** is the most widely used web server software. Developed and maintained by Apache Software Foundation, Apache is an open source software available for free.

*Install Apache using Ubuntu’s package manager ‘apt’:*

>#update a list of packages in package manager

sudo apt update

>#run apache2 package installation

sudo apt install apache2

>#After apache2 is successfully installed, verify that apache2 is running as a service on Ubuntu using the following commands

sudo systemctl status apache2
