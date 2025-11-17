# Hosting Wordpress Step-by-Step 

## Introduction  

This project offers a detailed walkthrough for launching a WordPress website on a server with Apache as the web server and MariaDB as the database. It covers setting up the environment, installing necessary components, configuring WordPress, and completing the deployment to make the site accessible online. By following this guide, you can achieve a secure, scalable, and production-ready WordPress setup.

## Prerequisites

Before launching the WordPress website, confirm that the following are set up and operational:

* Linux Server – Amazon Linux operating system

* Web Server – Apache installed and actively running

* PHP – Including all necessary PHP extensions

* Database – MariaDB installed for managing WordPress data

## Step-by-Step Setup

### Step 1: Launch an EC2 Instance and Connect Securely via SSH

1. Launch EC2 Instance

<p><img src="Image/instance launch.png" alt="Instance"></p>


2. Copy SSH Command

<p><img src="Image/ssh copy.png" alt="Instance"></p>

3. Paste it on Git bash terminal

<p><img src="Image/bird.png" alt="Instance"></p>



### Step 2: Automating the Installation of the LAMP Stack on an AWS EC2 Instance

1. Create a lamp.sh file

   #sudo vim lamp.sh


<p><img src="Image/vim cam.png" alt="Instance"></p>


2. Insert the script to install Apache, MySQL, and PHP on the system.

<p><img src="Image/vim open.png" alt="Instance"></p>








3. Open and run the file.

<p><img src="Image/bash lamp.png" alt="Instance"></p>

### Step 3: Downloading and Setting Up WordPress

1. Go to the html file
 
   #cd /var/www/html/


2. Download Wordpress

   #sudo wget https://wordpress.org/latest.tar.gz


3. Extract the archive

   #sudo tar -xvzf latest.tar.gz


<p><img src="Image/cd ls.png" alt="Instance"></p>



### Step 4: Remove latest.tar.gz

#sudo rm -rf latest.tar.gz

<p><img src="Image/ls rm -rf.png" alt="Instance"></p>



### Step 5: Go to the wordpress folder

#cd wordpress/

<p><img src="Image/cd wordpress.png" alt="Instance"></p>

### Step 6: Create a Database for WordPress


1. Create Username and Password

   #sudo mysql

   #alter user root@localhost identified by 'root';

<p><img src="Image/sudo mysql.png" alt="Instance"></p>


2. Login to Mysql (mariadb 105-server)

   #sudo mysql -u root -p

<p><img src="Image/sudo mysql password.png" alt="Instance"></p>



3. Create & Show Database

   #create database wordpressdb;

   #show databases;

<p><img src="Image/create show data word.png" alt="Instance"></p>


###  Step 7: Install Connector

     #sudo yum install php8.4-mysqlnd.x86_64


<p><img src="Image/php 8.4 install.png" alt="Instance"></p>





### Step 8: Change ownership of the files

    #sudo chown -R apache:apache wordpress/

 <p><img src="Image/chowm apache.png" alt="Instance"></p>          




###  Step 9: Copy the Public IP and Paste it in browser.   

1. Hit Pubilc IP on Browser


2. Click on continue

<p><img src="Image/english.png" alt="Instance"></p>  

3. Click on Let's go

<p><img src="Image/lets go.png" alt="Instance"></p>  

4. Fill all details and click on submit

<p><img src="Image/submit.png" alt="Instance"></p>  

5. Run the Installation

<p><img src="Image/run to installation.png" alt="Instance"></p>  

6. Fill up all information and click on install wordpress

<p><img src="Image/install wordpress.png" alt="Instance"></p> 



7. Login to wordpress


<p><img src="Image/login.png" alt="Instance"></p> 


8. Click on Login

<p><img src="Image/log in.png" alt="Instance"></p> 

9. Deployment of WordPress was successfull.

<p><img src="Image/welcome wdb.png" alt="Instance"></p> 

10. A new table was automatically inserted into the database.


<p><img src="Image/last show tables.png" alt="Instance"></p> 










## Project Summary

This project involves deploying a WordPress website on a Linux-based server using Apache as the web server and MariaDB as the database. It covers the complete setup process, including downloading WordPress, configuring file permissions, setting up the database, and optimizing the server for production. The result is a secure, scalable, and fully functional WordPress site accessible to the public.