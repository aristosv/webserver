# webserver

Nginx / Reverse Proxy / PHP / MariaDB / phpMyAdmin / LetsEncrypt / Fail2Ban / Portainer

This will install Swag, which includes the Nginx webserver, php, a reverse proxy, certbot for letencrypt certificates and fail2ban. It will also install MariaDB, phpmyadmin and portainer for container management. You can run it as root on a fresh, minimal installation of Debian.

```bash
bash <(wget --no-check-certificate -qO- https://raw.githubusercontent.com/aristosv/webserver/main/01_install)
```
After the installation, this is how you can access all the web apps:
```
Name: Portainer
Usage: container manager
URL: http://<your_ip_here>:9000
```
```
Name: phpMyAdmin
Usage: database manager
URL: http://<your_ip_here>:8112
```
