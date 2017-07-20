# pandora-docker-compose
Pandora FMS server instance composed and run by Docker with help of docker-compose. Compatible with Centos 6 and Docker-compose file v2.1.

dx* Includes Postfix service configuration for sending emails to the Pandora admins

Docker-compose creates a bridged network for the containers in the subnet 172.35.0.0/24. It is designed to work out-of-box but in case of changes in the network configuration, make sure to change server IP in the Postfix configuration under `server-config/postfix/main.cf`
