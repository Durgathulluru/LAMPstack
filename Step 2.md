# STEP 2 — INSTALLING MYSQL

Now that you have a web server up and running, you need to install a Database Management System (DBMS) to be able to store and manage
data for your site in a relational database. MySQL is a popular relational database management system used within PHP environments, 
so we will use it in our project.

Again, use ‘apt’ to acquire and install this software:

```
$ sudo apt install mysql-server
```

When prompted, confirm installation by typing Y, and then ENTER.

When the installation is finished, log in to the MySQL console by typing:


```
$ sudo mysql
```
You should see output like this:


```
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 8.0.22-0ubuntu0.20.04.3 (Ubuntu)

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> 
```

Set a password for the root user, using 
mysql_native_password as default authentication method. We’re defining this user’s password as PassWord.01.

```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';
```

Exit the MySQL shell with:

```
mysql> exit
```
It’s recommended that you run a security script that comes pre-installed with MySQL. This script will remove some insecure default 
settings and lock down access to your database system
Start the interactive script by running:

```
$ sudo mysql_secure_installation
```
Answer Y for yes, or anything else to continue without enabling.


```
VALIDATE PASSWORD PLUGIN can be used to test passwords
and improve security. It checks the strength of password
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD plugin?

Press y|Y for Yes, any other key for No:
```


If you answer “yes”, you’ll be asked to select a level of password validation. Keep in mind that if you enter 2 for the strongest
level, you will receive errors when attempting to set any password which does not contain numbers, upper and lowercase letters, 
and special characters, or which is based on common dictionary words e.g PassWord.1.


```
There are three levels of password validation policy:

LOW    Length >= 8
MEDIUM Length >= 8, numeric, mixed case, and special characters
STRONG Length >= 8, numeric, mixed case, special characters and dictionary              file

Please enter 0 = LOW, 1 = MEDIUM and 2 = STRONG: 1
```
```
$ sudo mysql -p
```


Notice the -p flag in this command, which will prompt you for the password used after changing the root user password.

To exit the MySQL console, type:

```
mysql> exit
```
