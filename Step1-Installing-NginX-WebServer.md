![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/01f8a2b1-844f-42ec-9d0e-dec7854aae96)

In order to display web pages to our site visitors, we are going to employ Nginx, a high-performance web server. We'll use the **apt** package.  

Since this is our first time using **apt** for this session, start off by updating your server's package index. Following that, you can use **apt install** to get Nginx
installed:  

```
$ sudo apt update  
$ sudo apt install nginx  
```
 
When prompted, enter **Y** to confirm that you want to install Nginx. Once installation is finished, the Nginx web server will be active and running on your Ubuntu 20.04 server.   

 To verify that nginx was succesfully installed and is running as a service in Ubuntu, run:  

```$ sudo systemctl status nginx```  

 If it is green and running then you did everything correctly - you have just launched your Web Server in the Cloud.  

 Before we can receive any traffice by our Web Server, we need to open **TCP port 80**   
