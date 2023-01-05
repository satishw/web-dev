# web-dev
Useful commands

## Apache Server
Start/stop/restart the Apache web server
```
sudo systemctl start httpd
```
```
sudo systemctl stop httpd
```
```
sudo systemctl restart httpd
```
Use the systemctl command to configure the Apache web server to start at each system boot. 
```
sudo systemctl enable httpd
```
You can verify that httpd is on by running the following command
```
sudo systemctl is-enabled httpd
```

## ssh login
```
ssh -i key.pem user@<server ip address>
```
## MySQL/MariaDB

Create database and add user
```
create database dbname;
```
```
grant usage on *.* to dbuser@localhost identified by 'password';
```
```
grant all privileges on dbname.* to dbuser@localhost ;
```
Flush the database privileges to pick up all of your changes.
```
flush privileges;
```

Import database
```
sudo mysql -u<dbuser> -p'password' dbname < backupdb.sql
```

Backup or export database
```
sudo mysqldump -u<dbuser> -p'password' dbname > backupdb.sql
```
```
sudo mysqldump --no-tablespaces -u<dbuser> -p'password' dbname > backupdb.sql
```
Start/stop/restart the MariaDB server
```
sudo systemctl start mariadb
```
```
sudo systemctl stop mariadb
```
```
sudo systemctl restart mariadb
```
Enable MariaDB server to start at every boot
```
sudo systemctl enable mariadb
```
You can verify that mariadb is on by running the following command
```
sudo systemctl is-enabled mariadb
```
