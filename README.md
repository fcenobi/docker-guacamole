Guacamole
====

Dockerfile for Guacamole 0.9.9 with embedded MariaDB (MySQL) Authentication

Guacamole is a clientless remote desktop gateway. It supports standard protocols like VNC and RDP.

---
Author
===

Based on the work of Zuhkov <zuhkov@gmail.com>
Updated by aptalca to the latest version of guacamole

---
Building
===

Build from docker file:

```
git clone https://github.com/fcenobi/docker-guacamole.git
docker build -t aptalca/guacamole .
```

You can also obtain it via:  

```
docker pull aptalca/guacamole
```

---
Running
===

Create your guacamole config directory (which will contain both the properties file and the database) and then launch with the following:

```
docker run -d -v /your-config-location:/config -p 8080:8080 aptalca/guacamole
```

Browse to ```http://your-host-ip:8080``` and login with user and password `guacadmin`

---
Credits
===

Guacamole is an open source project and is copyright Glyptodon LLC

This docker image is built upon the baseimage made by phusion and forked from hall/guacamole, and further forked from Zuhkov/docker-containers
