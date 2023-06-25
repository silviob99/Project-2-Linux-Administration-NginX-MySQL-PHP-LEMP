![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/0b949645-beee-43f5-973e-98764c9efe68)

Now that we have a web server up and running, you need to install a  [Database Management System (DBMS)](https://www.ibm.com/docs/en/zos-basic-skills?topic=zos-what-is-database-management-system) to be able to store andmanage data for your site in a [relational database](https://www.oracle.com/uk/database/what-is-a-relational-database/). [MySQL](https://dev.mysql.com/doc/refman/8.0/en/what-is-mysql.html) is a popular relational database management system used within PHP environments, so we will use it in our project. 

Again use **apt** to acquire and install software:  

```$ sudo apt install mysql-server```  

When prompted, confirm installation by typing **Y** and then **ENTER**.  

When installation is finsihed, it's recommended that you run a security script that comes preinstalled with MySQL. This script will remove some insecure default settings and lock down access to your database system. start interactive script by running:  

```$ sudo mysql_secure_installation```  

This will ask if you want to configure the ```VALIDATE PASSWORD PLUGIN```  

``` **Note:** Enabling this feature is something of a judgment call. If enabled, passwords which```

Answer **Y** for yes, or anything else to continue without enabling.  

```
VALIDATE PASSWORD PLUGIN canbe used to test passwords
and improve security. It checks the strength of password  
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD plugin?
Press y|Y for Yes, any other key for No:
```  
If you answer "yes", you'll be asked to select a level of password validation. Keep in mind that if you 
enter **2** for the strongest level, you will receive errors when attempting to set any password, which does not contain numbers, upper and lowercase letters, and special characters, or which is based on common dictionary words. 

```
There are three levels of password validation policy:

LOW     Length >= 8 
MEDIUM  Length >= 8 numeric, mixed case, and special characters
HIGH    Length >= 8 numeruc, mixed case, special characters and dictionary file

Please enter 0 = LOW, 1 = MEDIUM and 2 = STRONG: 1
```

