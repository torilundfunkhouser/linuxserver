Overview of Project
This project — Linux Server Configuration — is the final project in the Udacity Full Stack Nanodegree program. The main objective of this project was to set up a Linux server with good security settings and a running web server, which runs the Item Catalog project.


I created a Linux Ubuntu virtual environment on AWS and configured the server to safely host my catalog project, which allows user to log in and save content recommendations for streaming sites such as Netflix, Hulu, HBO Go, etc. The SSH port is 2200, as specified in the project rubric. 


The public IP address is 54.191.247.202, and URL is torifunkhousercontentrecommendations.xyz. 


Summary of software installed
To run the catalog application, I installed: Flask, httplib2, oauth2client, sqlalchemy, psycopg2, requests. I also installed virtualenv to isolate installation of the Python packages required to run the app from the rest of the site directories. In addition, I installed libpq-dev python-dev and postgresql to connect to the PostgreSQL database.


To run the app via apache, I installed apache2 and libapache2-mod-wsgi.


I also installed git to clone my catalog app from my git repository — and pip to more easily install software.


Summary of configurations made
As specified in the rubric, I added grader user and gave grader user sudo access — as well as ownership of the catalog application and .ssh keys. After that, I disabled root access to the server and disabled ssh login for the root user. I also disabled ssh port 22 (changing it to port 2200), and added udp port 123. 


I also added the configuration for my custom domain name (torifunkhousercontentrecommendations.xyz) in the catalog.conf and /etc/hosts file.


Resources
Helpful resources I used to complete this project include the following:
* How to Set Up Virtual Hosts on Ubuntu
* Creating User, Database, and adding access on PostgreSQL
* How I Deployed a Flask App Using Lightsail on Amazon Web Service
* mod_wsgi (Apache)
* Flask Hello world App with Apache WSGI
* Creating a DNS zone to manage your domain’s DNS records in Amazon Lightsail
* Creating a simple website with a custom domain on Amazon Lightsail + Docker
* Udacity Knowledge post RE javascript origins + xip.io