# MariaDB


### Installation tip

* After installing mariadb, please initiate the db and then start the database
	- `mysql_install_db --user=mysql --basedir=/usr --datadir=/var/lib/mysql`


### MariaDB Setup

* `mysql_secure_installation`

### Creating Users and Databases

* How to access database
	- `mysql -u username -p`
		+ You will be promted for password

* After logging in to the db, 
	- `create database db_name;`
	- `show databases;`
	- `create user username@localhost identified by 'password';`
	- `select user from mysql.user;`
	- `grant all privileges on db_name.* to user@localhost identified by 'password';`
	- `flush privileges;`

### Remove users and databases

* `show grants for 'username@localhost';`
* `revoke all privileges, grant option from user@localhost`
* `drop user  if exists username@localhost`
* `drop database if exists db_name`
