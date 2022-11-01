# UbuntuCodes

```bash
 sudo apt update 
 sudo apt upgrade 
 sudo apt install mysql-server mysql-client 


```
1. Yol
```bash
 sudo mysql_secure_installation
```

2. Yol
```bash
ALTER USER ‘kullanıcıAdi’@’staticIP’IDENTIFIED WITH mysql_native_password BY ‘şifre;
```

```bash
sudo ufw enable //firewall
sudo ufw allow 3306/tcp //mysql port
sudo ufw allow 3306/tcp
sudo ufw allow 22/tcp //ssh port
```

```bash
cd /etc/mysql/mysql.conf.d
nano mysqld.cnf 
```
> bind-address = 0.0.0.0 yap
```bash
sudo systemctl start mysql
sudo systemctl enable mysql
sudo systemctl restart mysql 
```

```bash
mysql -u root -p
create database test;
CREATE USER 'new_user’@‘staticIp’ IDENTIFIED BY 'new_password';
GRANT ALL ON my_db.* TO 'new_user’@’staticIp;
FLUSH PRIVILEGES;
```
