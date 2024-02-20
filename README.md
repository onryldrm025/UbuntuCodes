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
bind-address = 0.0.0.0 yap
```

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

# Nginx

```bash
sudo apt install nginx
sudo systemctl start nginx
sudo systemctl enable nginx
sudo systemctl restart nginx
sudo ufw allow 'Nginx Full' 
sudo ufw enable // dikkat et ssh acik degilse 
nginx -v

 server {
  listen 80;
  listen [::]:80;
  server_name www.deneme.com deneme.com

  location / {
      proxy_pass http://localhost:3040;
      proxy_set_header Host $host;
      proxy_set_header X-Real-IP $remote_addr;
      proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
      
  }
}
nginx -t
```
