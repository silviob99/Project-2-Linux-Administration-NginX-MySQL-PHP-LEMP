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

Regardless of wheather you chose to set up the ```VALIDATE PASSWORD PLUGIN```, your server will next ask you to select and confirm a password for the MySQL **root** user. This is not to be confused with the **system root**. The **database root** user is an administrative user with full privileges over the database system. even though the default authentiction method for the MySQL root user dispenses the use of a password. **even when one is set**, you should define a strong password here as an additional   
safety measure. I'll talk about this in a moment.  

It you enabled password validation, you'll be shown the password strength for the root password you just entered and your server will ask if you want to continue with that password. If you are happy with your current password, enter Y for "yes" at the prompt:  

```
Estimated strength of the password: 100 
Do you wish to continue with the password provided?(Press y|Y for Yes, any other key for No) : Y
 ... Failed! Error: Your password does not satisfy the current policy requirements
```

For the rest of questions, press ```Y``` and hit the ```ENTER``` key to each prompt. This will remove some anonymous users and the test database, disable remote root logins, and load these new rules so that MySQL immediately respects the changes you have made.  

When you're finished, test if you're able to log in to the MySQL console by typing:  

```$ sudo mysql```  
