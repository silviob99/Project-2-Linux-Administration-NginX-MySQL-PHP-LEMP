![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/1007a286-9792-4071-8270-9df204f8afec)

In this step you will create a test database (DB) with simple "To do list" and onfigure access to it, so the Nginx website would be able to query data from the DB and display it.  

At the time of this writing, the native MySQL PHP library ```mysqlnd``` doesn't support ```catching_sha2_authentication```, the default authentication method for MySQL 8. We'll need to create a new user with the ```mysql_native_password``` authentication method in order to be able to connect to the MySQL database from PHP.  

I will create a database named **example_database** and a user named **example_user**, but you can replace these names with different values.  

First I will connect to the MySQL console using the **root** account:  

```
$ sudo mysql
```

To create a new database, run the following command from your MySQL console:  

```
mysql> CREATE DATABASE `example_database`;
```

Now you can create a new user and grant him full privileges on the database you have just created.  

The following command creates a new user named ```example_user```, using mysql_native_password as default authentication method. We're defining this user's password as ```password```, but you should replace this value with a secure password of your own choosing.  

```
mysql> CREATE USER 'example_user'@'%' IDENTIFIED WITH mysql_native_password BY 'password';

```
Now we need to give this user permission over the ```example_database``` database:    

```
mysql> GRANT ALL ON example_database.* TO 'example_user'@'%';
  
```

This will give the **example_user** user full privileges over the **example_database** database, while preventing this user from creating or modifying other databases on your server.  

Now exit the MySQL shell with:  

```
mysql> exit
```

You can test if the new user has the proper permissions by logging in to the MySQL console again, this time using the custom user credentials:  


