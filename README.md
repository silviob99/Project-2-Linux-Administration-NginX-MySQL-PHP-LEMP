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
Project Overview
Project-2: Web Stack Implementation (LEMP) is a tutorial-based project that guides users through the process of setting up a LEMP (Linux, Nginx, MySQL, PHP) web stack on Ubuntu 20.04. This project aims to provide a step-by-step guide for beginners to learn how to install and configure the essential components of a web server.

### Prerequisites
Before starting the installation process, ensure that you have the following prerequisites:  

- An AWS account
- A virtual server with Ubuntu Server OS  

### Installation
To install and set up the LEMP stack on Ubuntu 20.04, follow these steps:

Step 0: Preparing Prerequisites ](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/blob/main/Step0-Preparing-Prerequisits.md)
- Create an AWS account if you don't have one.
- Launch an EC2 instance of the t2.nano family with Ubuntu Server 20.04 LTS (HVM) image.


Step 0: Preparing Prerequisites
- Create an AWS account if you don't have one.
- Launch an EC2 instance of the t2.nano family with Ubuntu Server 20.04 LTS (HVM) image.

Step 1: Installing Nginx Web Server
- Install Git Bash.
- Launch Git Bash and run the following command to connect to your EC2 instance: `ssh -i <Your-private-key.pem> ubuntu@<EC2-Public-IP-address>`.
- Install Nginx using the apt package manager.
- Verify that Nginx is running by checking its status.

Step 2: Installing MySQL
- Install MySQL using the apt package manager.
- Run the MySQL security script to secure your MySQL installation.
- Test if you can log in to the MySQL console.

