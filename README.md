# webserver

Nginx / PHP / MariaDB / phpMyAdmin / LetsEncrypt / Fail2Ban / Portainer
---

This will install the [Swag](https://docs.linuxserver.io/images/docker-swag) container, which includes the Nginx webserver, php, a reverse proxy, certbot for letsencrypt certificates and fail2ban for intrusion prevention. It will also install MariaDB, phpMyAdmin, Portainer for container management and WordPress. Everything will be installed in a containerized environment.

Before running the script you will have to open ports 80 and 443 on your firewall, to allow http to https redirection and certificate validation. You will also have to create an A record for your domain and point it to your server IP Address. Setup will not continue if the A record does not match your server IP Address.

---
## Required setup information
- **Domain Name:** The name of the domain you want to host on your server.
- **Email Address:** Your email address, used for LetsEncrypt notifications.
---
## Install
You can run the command below as root on a fresh, minimal installation of Debian.
```bash
bash <(wget --no-check-certificate -qO- https://raw.githubusercontent.com/aristosv/webserver/main/01_install)
```
---
- The script will install Docker, all the containers, create a new database and download WordPress.
- After the installation you can visit your domain and setup WordPress.
- Necessary passwords will be automatically generated during setup and will be reported at the end.
- You can also manage the containers and the database with the tools below.
```
Name: Portainer
Usage: container manager
URL: http://server_lan_ip:9000
```
```
Name: phpMyAdmin
Usage: database manager
URL: http://server_lan_ip:8082
```
---
## Update
To update your system and all the containers you can run the following command
```bash
bash <(wget --no-check-certificate -qO- https://raw.githubusercontent.com/aristosv/webserver/main/11_install_update)
```
---
