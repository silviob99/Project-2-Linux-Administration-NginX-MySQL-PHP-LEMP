![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/33b729a4-71a0-4c11-a6cd-c641dc87b29c)

I have Nginx installed to serve my content and MySQL installed to store and manage my data. Now Ican call PHP to process code and generate dynamic content for the web server. 

While Apache embeds the PHP interpreter in each request, Nginx requires an external program to handle PHP processing and act as a bridge between the PHP interpreter itself and the web server. This allows for a better overall performance in most PHP-based websites, but it requires additional configuration. You'll need to install ```php-fpm```, which stands for "PHP fastCGI process manager", and tell Nginx to pass PHP requests to this software for processing. Additionally, you'll need ```php-mysql```,   
a PHP module that allows PHP to communicate with MySQL-based databases. Core PHP packages will automatically be installed as dependencies. 

To install these 2 packages at once, run:  

```
$ sudo apt install php-fpm php-mysql
```

When prompted, type ```Y``` and press ```ENTER``` to confirm installation.  

I now have my PHP components installed. Next, I will configure Nginx to use them.  

