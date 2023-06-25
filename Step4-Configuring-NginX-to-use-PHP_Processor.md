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

Then, open a new configuration file in Nginx's ```sites-available``` directory using your preffered command-line editor. Here, we'll use ```nano```:

```
$ sudo nano /etc/nginx/sites-available/projectLEMP
```

This will create a new blank file. Paste in the following bare-bones configuration:  

```
#/etc/nginx/sites-available/projectLEMP

server {
      listen 80;
      server_name projectLEMP www.projectLEMP;
      root /var/www/projectLEMP;

      index index.html index.htm index.php;

      location / {
          try_files $uri $uri/ =404; 
}

location ~ \.php$ {
      include snippets/fastcgi - php.conf;
      fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
}

location ~ /\.ht {
      deny all;
      }
}
```

Here's what each of these directives and location blocks do:

* ```listen``` -Defines what port Nginx will listen on. In this case, it will listen on port ```80```, the default port for HTTP.
* ```root``` -Defines the document root where the files served by this website are stored.
* ```index``` -Defines in which order Nginx will prioritize index files for this website. It is a common practice to list ```index.html``` files with a higher precedence than ```index.php``` files to allow for quickly setting up a maintenance landing page in PHP applications. You can adjust these settings to better suit your application needs.
* ```server_name``` -Defines which domain names and/or IP addresses this server block should respond for. **Point this directive to your server's name or public IP address**.
* ```location /``` - The first location block includes a ```try_files``` directive, which checks for the existence of files or directories matching a URL request. If Nginx cannot find the appropriate resource, it will return a 404 error.
* ```location ~ \.php$``` -This location block handles the actual PHP processing by pointing Nginx to the fastcgi-php.conf configuration file and the ```php7.4-fpm.sock file```, which declares what socket is associated with ```php-fpm```.
* ```location ~ /\.ht``` -The last location block deals with ```.htaccess``` files, which Nginx does not process. By adding the deny all directive, if any ```.htaccess``` files happen to find their way into the document root, they will not be served to visitors.

When you're done editing, save and close the file. If you're using ```nano```, you can do so by typing ```CTRL+X``` and then ```y``` and ```ENTER``` to confirm.  

