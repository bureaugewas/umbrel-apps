##Connect to db via terminal (umbrel):
docker exec -it <mysql_db_1> mysql --user root -ppassword

##Create a new user
CREATE USER 'umbrel'@'192.168.2.49' IDENTIFIED BY '123';
Query OK, 0 rows affected (0.045 sec)

MariaDB [mysql]> GRANT ALL PRIVILEGES ON *.* TO 'umbrel'@'192.168.2.49' WITH GRANT OPTION;
Query OK, 0 rows affected (0.042 sec)

MariaDB [mysql]> FLUSH PRIVILEGES;

logging in takes a few tries, and automatically logs out for some reason