![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/1007a286-9792-4071-8270-9df204f8afec)

In this step you will create a test database (DB) with simple "To do list" and onfigure access to it, so the Nginx website would be able to query data from the DB and display it.  

At the time of this writing, the native MySQL PHP library ```mysqlnd``` doesn't support ```catching_sha2_authentication```, the default authentication method for MySQL 8. We'll need to create a new user with the ```mysql_native_password``` authentication method in order to be able to connect to the MySQL database from PHP.  

I will create a database named **example_database** and a user named **example_user**, but you can replace these names with different values.  

First I will connect to the MySQL console using the **root** account:  

```
$ sudo mysql
```



