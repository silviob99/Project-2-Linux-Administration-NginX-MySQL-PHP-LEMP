![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/8fd76e69-05c6-4b67-a9a9-25057b395b88)

LEMP stack should be completely set up.  

At this point, your LEMP stack is completely installed and fully operational.  

I will test it to validate that Nginx can correctly hand ```.php``` files off to my PHP processor.  

I will do this by creating a test PHP file in my document root. Open a new file called ```info.php```  
within my document root in my text editor:  

```
$ nano /var/www/projectLEMP/info.php
```

Type or paste the following  lines into the new file. This is valid PHP code that will return 
information about my server:  

```
<?php
phpinfo();
```

I can now access this page in my web browser by visiting the domain name or public IP address that I have set up in my Nginx configuration file, followed by ```/info.php:```  

<img width="570" alt="PHP-frontpage" src="https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/1c32a4a8-816d-4260-a2b7-c8078441724e">

After checking the relevant information about your PHP server through that page, it's best to remove the file you created as it contains sensitive information about your PHP environment and your Ubuntu server. You can use ```rm``` to remove that file:  

```
$ sudo rm /var/www/your_domain/info.php
```

You can always regenerate this file if you need it later.  


