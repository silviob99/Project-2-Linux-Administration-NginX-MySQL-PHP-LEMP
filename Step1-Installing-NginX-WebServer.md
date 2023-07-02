![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/56ebde15-cec8-455f-a80b-d8cb09c4c641)


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

 Before we can receive any traffice by our Web Server, we need to open **TCP port 80** which is default port that web browsers use to access web pages in the Internet.

As we know, we have TCP port 22 open by default on our EC2 machine to access it via SSH, so we need to add a rule to EC2 configuration to open inbound connection through port 80.   


https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/d2686901-648a-42bd-af07-0b6ed72e6164


Our server is running and we can access it locally and from the Internet (Source 0.0.0.0/0) means 'from any IP address').  

first, let us try to check how we can access it locally in our Ubuntu shell, run:

```
$ curl http://localhost:80
or
$ curl http://127.0.0.1:80
```
We should get this screen:  

 <img width="960" alt="is-nginx-running-test" src="https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/37f2e6fd-c421-489d-aaac-25da7fdffb7b">  

These 2 commands above actually do pretty much the same - they use 'curl' command to request our Nginx on port 80 (you can even try to not specify any port - it will work anyway). The difference is that: in the first case we try to access our server via [DNS name](https://www.cloudflare.com/en-gb/learning/dns/what-is-dns/) and in the second one - by IP address (in this case IP address 127.0.0.1 corresponds to DNS name 'localhost' and the process of converting a DNS name to IP is called "resolution"). I will touch DNS in further lectures and projects.  

As an output you can see some strangely formatted test, do not worry, we just made sure that our Nginx web service responds to 'curl' command with some payload.  

Now it's time for us to test  how our Nginx server can respond to requests from the Internet. Open a web browser of your choice and try access following url  

```http://<Public-IP-Address>:80```  

Another way to retrieve your Public IP address, other than to check it in AWS Web console, is to use following command:  

```curl -s http://169.254.169.254/latest/meta-data/public-ipv4```  

The URL in browser shall also work if you do not specify port number since all web browsers use port 80 by default.  

If you see following page, then your web server is now correctly installed and accessible through your firewall.  

<img width="434" alt="Nginx-welcome-page" src="https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/252d72bf-de4f-4285-8894-860e2f0fba73">   

In fact, it is the same content that you previously got by 'curl' command, but represented in HTML formatting by your web browser.  



