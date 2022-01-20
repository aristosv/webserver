# webserver

Nginx / Reverse Proxy / PHP / MariaDB / phpMyAdmin / LetsEncrypt / Fail2Ban / Portainer

This will install Swag, which includes the Nginx webserver, php, a reverse proxy, certbot for letencrypt certificates and fail2ban. It will also install MariaDB, phpmyadmin and portainer for container management. You can run it as root on a fresh, minimal installation of Debian.

```bash
bash <(wget --no-check-certificate -qO- https://raw.githubusercontent.com/aristosv/webserver/main/01_install)
```
