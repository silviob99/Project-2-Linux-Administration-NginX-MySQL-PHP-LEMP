![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/0b949645-beee-43f5-973e-98764c9efe68)

Now that we have a web server up and running, you need to install a  [Database Management System (DBMS)](https://www.ibm.com/docs/en/zos-basic-skills?topic=zos-what-is-database-management-system) to be able to store andmanage data for your site in a [relational database](https://www.oracle.com/uk/database/what-is-a-relational-database/). [MySQL](https://dev.mysql.com/doc/refman/8.0/en/what-is-mysql.html) is a popular relational database management system used within PHP environments, so we will use it in our project. 

Again use **apt** to acquire and install software:  

```$ sudo apt install mysql-server```  

When prompted, confirm installation by typing **Y** and then **ENTER**.  

When installation is finsihed, it's recommended that you run a security script that comes preinstalled with MySQL. This script will remove some insecure default settings and lock down access to your database system. start interactive script by running:  

```$ sudo mysql_secure_installation```  

This will ask if you want to configure the ```VALLIDATE PASSWORD PLUGIN```  


