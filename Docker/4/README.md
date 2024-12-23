# Administrar mis Contenedores desde mi Teléfono Móvil
## Este video aprenderemos como administrar con una herramienta nuestros contenedores de Docker



### crear conexion ssh con docker

### paso 1
verificamos que sericios este en la red
netstat -tulpn

sino funciona insstamos esto
apt install net-tools

vamos a editar el servicop de docker, para ello ingresamos aca y editamos con nano/etc/docker/daemon

### paso 2

luego modificamos esta linea
nos ubicamos en esta linea:

ExecStart=/usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock

y la dejamos de esta forma

ExecStart=/usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock -H=tcp://0.0.0.0:2375

### paso 3

reiniciamos 2 servicios el primero

systemctl daemon-reload
systemctl restart docker.service

con eso ya deveria estar

#### paso 4:

verificacion que podamos ingresar a la pagina web, colocando tu direccion de tu portainer

http://0.0.0.0:2375/
deveria aparecer asi

{"message":"page not found"}

y ya con eso verificamos que accedamos a la red
