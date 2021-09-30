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

`sudo apt update`

>#run apache2 package installation

`sudo apt install apache2`

>#After apache2 is successfully installed, verify that apache2 is running as a service on Ubuntu using the following commands

`sudo systemctl status apache2`

The output is similar to the below screenshot

![apache-verification](https://user-images.githubusercontent.com/40571508/135532326-9e51a794-0b05-4c54-a1e5-90cb0d4465af.PNG)

>#To access the Web server locally, run the below commands-This shows the same output.

 `curl http://localhost:80`
 
or

 `curl http://127.0.0.1:80`
 
 Webserver sample output
 
 ![webserver-sample-output](https://user-images.githubusercontent.com/40571508/135535323-23e4dfe9-7a3b-4822-853d-04cdacab269b.PNG)
 
 >Need to test how our Apache HTTP server can respond to requests from the Internet?
 >Open a web browser of your choice and try to access following url
 
 `http://<Public-IP-Address>:80`
 
 >To retrieve the public IP without accessing AWS console, run the command below.
 
 `curl -s http://169.254.169.254/latest/meta-data/public-ipv4`
 
 #The below output shows that the web server is now correctly installed and accessible through your firewall.
 
 STEP 2 — INSTALLING MYSQL
 
 >#Again, use ‘apt’ to acquire and install this software:

 `sudo apt install mysql-server`
 
 >#When this is successfully setup, test if you’re able to log in to the MySQL console by typing:
 
 `sudo mysql`
 
 ![mysql-output](https://user-images.githubusercontent.com/40571508/135538204-484b3651-844e-47ec-a62e-d16b089206a1.PNG)
 
 STEP 3 — INSTALLING PHP
 
>PHP is the component of our setup that will process code to display dynamic content to the end user. In addition to the php package, you’ll need php-mysql, a PHP module that allows PHP to communicate with MySQL-based databases. You’ll also need libapache2-mod-php to enable Apache to handle PHP files. Core PHP packages will automatically be installed as dependencies.

>#To install the 3 packages at once, run:

`sudo apt install php libapache2-mod-php php-mysql`

At this point, your LAMP stack is completely installed and fully operational.

- Linux (Ubuntu)
- Apache HTTP Server
- MySQL
- PHP


 
 
 ☕ credits [Darey.io Website](https://www.darey.io/) & [Apache website](https://www.apache.org/)
