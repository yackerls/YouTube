# Como Actualizar PORTAINER Versión 2.21. 5  y Todas las Versiones
## En este video traigo como actualizar portainer.

pasos:

docker ps -a

docker images

docker stop portainer

docker rm portainer

    docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:2.21.5
    

➡️link de documentación: https://docs.portainer.io/start/install-ce/server/docker/linux