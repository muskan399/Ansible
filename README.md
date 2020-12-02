# Ansible
Examples of playbooks that we can use for automation in configuration management.

> ## Key points for docker_webserver.yml:
1. To copy file in /var/www/html folder of container we used the concept of volumes. Volumes created using Docker always takes space from Docker host and creates a folder /var/lib/docker/volumes/volume_name/_data so here we first copied data from controller node and stored in this _data folder which we then mounted on the folder in container.

2. Here we mount the volume on /usr/local/apache2/htdocs/ but not on /var/www/html because whenever we update some code we need to restart the services and restart command behind the scene get files from /usr/local/apache2/htdocs/ folder so here we directly updated it so we don't need to restart the httpd services.
