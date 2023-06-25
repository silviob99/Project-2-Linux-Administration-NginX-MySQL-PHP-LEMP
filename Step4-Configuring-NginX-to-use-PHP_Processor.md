![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/3275435e-e0bd-4ef1-a8a9-d5e36efbde81)

When using the Nginx web server, we can create server blocks (similar to virtual hosts in Apache) to encapsualte configuration details and host more than one domain on a single server. In this guide, we will use **projectLEMP** as an example domain name. 

On Ubuntu 20.04. Nginx has one server block enabled by default and is configured to serve documents out of directory at ```/var/www/html```. While this world well for a single site, it can become difficult to manage if you are hosting multiple sites. Instead of modifying ```/var/www/html```, we'll create a directory structure within ```/var/www```  
for the **your_domain** website, leaving ```/var/www/html``` in place as the default directory to be served if a client request does not match any other sites.  

Create the root web directory for **your_domain** as follows:  

```
$ sudo mkdir /var/www/projectLEMP
```

Next, assing ownership of the directory with the $USER environment variable, which will reference your current system user:  

```
$ sudo chown -R $USER:$USER /var/www/projectLEMP 
```

