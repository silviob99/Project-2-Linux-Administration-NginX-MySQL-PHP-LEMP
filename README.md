![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/fb575d02-4983-43b5-a783-1f390d193353)

# Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP
LEMP stack: Linux OS, Nginx web server, MySQL database, PHP scripting language. It's a powerful combo for hosting dynamic websites, ensuring high performance and scalability.

Project 2 - Nginx, MySQL, PHP (LEMP) Web Stack Implementation
This project provides a step-by-step guide on setting up a LEMP (Linux, Nginx, MySQL, PHP) web stack on an Ubuntu 20.04 server.

### Table of Contents
- Project Overview
- Installation
- Usage
- Steps

### Project overview  
Project-2: Web Stack Implementation (LEMP) is a tutorial-based project that guides users through the process of setting up a LEMP (Linux, Nginx, MySQL, PHP) web stack on Ubuntu 20.04. This project aims to provide a step-by-step guide for beginners to learn how to install and configure the essential components of a web server.

### Prerequisites
Before starting the installation process, ensure that you have the following prerequisites:  

- An AWS account
- A virtual server with Ubuntu Server OS  

### Installation
To install and set up the LEMP stack on Ubuntu 20.04, follow these steps:

### Steps

#### Step 0: Preparing Prerequisites
- Create an AWS account if you don't have one.
- Launch an EC2 instance of the t2.nano family with Ubuntu Server 20.04 LTS (HVM) image.

#### Step 1: Installing Nginx Web Server
- Install Git Bash.
- Launch Git Bash and run the following command to connect to your EC2 instance: `ssh -i <Your-private-key.pem> ubuntu@<EC2-Public-IP-address>`.
- Install Nginx using the apt package manager.
- Verify that Nginx is running by checking its status.

#### Step 2: Installing MySQL
- Install MySQL using the apt package manager.
- Run the MySQL security script to secure your MySQL installation.
- Test if you can log in to the MySQL console.

#### Step 3: Installing PHP
- Install PHP using the apt package manager.
- Verify the PHP installation.

#### Step 4: Configuring Nginx to Use PHP Processor
- Configure Nginx to use PHP-FPM to process PHP files.

#### Step 5: Testing PHP with Nginx
- Create a test PHP file and verify that it's being served correctly by Nginx.

#### Step 6: Retrieving Data from MySQL Database with PHP
- Connect to the MySQL database using PHP and retrieve data.

### Usage
Once the LEMP stack is set up, you can use it to host and run web applications. To test if your installation is successful, you can access your website using the public IP address of your EC2 instance.

### Steps

- **Step 0:** [Preparing Prerequisites](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/blob/main/Step0-Preparing-Prerequisits.md)
- **Step 1:** [Installing Nginx Web Server](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/blob/main/Step1-Installing-NginX-WebServer.md)
- **Step 2:** [Installing MySQL](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/blob/main/Step2-Installing-MySQL.md)
- **Step 3:** [Installing PHP](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/blob/main/Step3-Installing-PHP.md)
- **Step 4:** [Configuring Nginx to Use PHP Processor](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/blob/main/Step4-Configuring-NginX-to-use-PHP_Processor.md)
- **Step 5:** [Testing PHP with Nginx](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/blob/main/Step5-Testing-PHP-with-NginX.md)
- **Step 6:** [Retrieving Data from MySQL Database with PHP](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/blob/main/Step6-Retrieving-data-from-MySQL-database-with-PHP.md)
