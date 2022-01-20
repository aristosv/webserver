# webserver

Nginx / Reverse Proxy / PHP / MariaDB / phpMyAdmin / LetsEncrypt / Fail2Ban / Portainer

This will install Swag, which includes the Nginx webserver, php, a reverse proxy, certbot for letencrypt certificates and fail2ban. It will also install MariaDB, phpmyadmin and portainer for container management. You can run it as root on a fresh, minimal installation of Debian.

Before running the script you will have to open ports 80 and 443 on your firewall, to allow http > https redirection and certificate validation. You will also have to create an A record for your domain and point it to your server IP Address.

---
## Required setup information
- **Domain Name:** The name of the domain you want to host on your server, without www.
- **Email Address:** Your email address, used for LetsEncrypt notifications
- **MariaDB root Password:** The root password for your MariaDB database

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
