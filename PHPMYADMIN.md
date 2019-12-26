Debian Stretch - dropar usuario root sem senha na table user

> DROP USER 'root'@'localhost';


> CREATE USER 'root'@'%' IDENTIFIED BY '12345678';

> GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'password' WITH GRANT OPTION;

> GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost' IDENTIFIED BY 'password' WITH GRANT OPTION;

> FLUSH PRIVILEGES;
