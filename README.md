# webserver

Nginx / Reverse Proxy / PHP / MariaDB / phpMyAdmin / LetsEncrypt / Fail2Ban / Portainer

This will install the [Swag](https://docs.linuxserver.io/images/docker-swag) container, which includes the Nginx webserver, php, a reverse proxy, certbot for letsencrypt certificates and fail2ban. It will also install MariaDB, phpMyAdmin and Portainer for container management. Everything will be installed in a containerized environment.

Before running the script you will have to open ports 80 and 443 on your firewall, to allow http to https redirection and certificate validation. You will also have to create an A record for your domain and point it to your server IP Address.

---
## Required setup information
- **Domain Name:** The name of the domain you want to host on your server.
- **Email Address:** Your email address, used for LetsEncrypt notifications.
- **MariaDB root Password:** The root password for your MariaDB database.
---
You can run the command below as root on a fresh, minimal installation of Debian.
```bash
bash <(wget --no-check-certificate -qO- https://raw.githubusercontent.com/aristosv/webserver/main/01_install)
```
---
After the installation, this is how you can access the web apps:
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
