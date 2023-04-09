# INSTRUCTION MANUAL 
## INSTALL AND EXECUTE MYSQL
1. Enter the ```brew install mysql``` in terminal to inatll mysql

2. Enter the ```brew services start mysql``` to start mysql

I got the error ```Error 2002 (HY000): socket '/tmp/mysql.sock' (2)``` and this was because I did not started the mysql to use mysql command

referred to the stack overflow post
https://stackoverflow.com/questions/15450091/error-2002-hy000-cant-connect-to-local-mysql-server-through-socket-tmp-mys

3. Enter the ```mysql_secure_installation`` to set settings. Sooa, you bettter not forget the password🫠

4. ```mysql -u root -p``` to execute the mysql. 

---
## GENERAL COMMAND
To understand easily, think database as a directory, and think tables as a files. 
Usually type 

### Database
 - Create database: <br>
    ```CREATE DATABASE `database_name` CHARACTER SET utf8 COLLATE utf8_general_ci;```
 - Show databases: <br>
    ```SHOW databases;``` 
 - Delete database: <br> 
    ```DROP DATABASE `database_name`;```
 - Read database: <br>
    ```use databases_name;```

### Table
 - Create table: <br>
    ```CREATE TABLE `table_name` (  ```
    ```column1` datatype(size) data_exsistance,``` <br>
    ```column2` datatype(size) data_exsistance,``` <br>
    ```) ENGINE=InnoDB DEFAULT CHARSET=utf8;```

    Example: <br>
    ``CREATE TABLE `table_name` (  ```
    ```id` int(11) NOT NULL AUTO_INCREMENT, ``` <br> 
    ```title` varchar(100) NOT NULL,  ``` <br>
    ```description` text NOT NULL, ``` <br>
    ```author` varchar(30) NOT NULL, ``` <br>
    ```created` datatime NOT NULL, ``` <br>
    ```PRIMARY KEY(id) ``` <br>
    ```) ENGINE=InnoDB DEFAULT CHARSET=utf8; ```

     AUTO_INCREAMENT: add unique number automatically when a new record is inserted into a table.
` 
 - Show tables: <br>
    ```SHOW databases;```
 - Read table: <br>
    ```SELECT column FROM table_name```

    Example: <br>
    ```SELECT * FROM table_name```
    ```SELECT id, title, author FROM topic``` <br> 
    ```SELECT id, title, author * topic ORDER BY id DESC``` 
    ```SELECT id, title, author * topic ORDER BY author DESC``` 

    *: indicats all

 - Insert data: <br>
    ```INSERT INTO table_name VALUES (value1, value2, value3,...)``` <br>
    ```INSERT INTO table_name (column1, column2, column3,...) VALUES (value1, value2, value3,...)```
    
    Example: <br>
    ```INSERT INTO `topic` VALUES ('1984', 'dystopian social science fiction novel', 'George Orwell', 'June 8, 1949');``` <br>
    ```INSERT INTO `topic` (`id`, `name`, `sex`, `address`, `birthday`) VALUES ('Animal Farm', 'satirical allegorical novel', 'George Orwell', '17 August 1945');```


