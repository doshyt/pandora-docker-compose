# pandora-docker-compose
Pandora FMS server instance composed and run by Docker with help of docker-compose. Compatible with Centos 6 and Docker-compose file v2.1.

* Allows to store Pandora Server DB files on the Docker host by mapping the DB data folder to lcoal.
* Includes Postfix service configuration for sending emails to the Pandora admins.
* Syncronizes docker host time with container via mapping `/etc/localtime` to containers.

Docker-compose creates a bridged network for the containers in the subnet 172.35.0.0/24. It is designed to work out-of-box but in case of changes in the network configuration, make sure to change server IP in the Postfix configuration under `server-config/postfix/main.cf`

How to start the server:
1. Copy files to target docker host.
2. Create empty folder `./db`
3. `docker-compose up`

To bring it down (it destroys containers!):
1. `docker-compose down`
