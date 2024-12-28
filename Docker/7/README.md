# Conectate a tus Equipos de Manera remota desde cualquier parte del mundo sin programas, con "guacamole"
### Apache Guacamole es una plataforma de acceso remoto basada en web que permite a los usuarios conectarse a sus escritorios o servidores a través de un navegador web, sin necesidad de instalar clientes adicionales. Guacamole proporciona acceso a varios protocolos de acceso remoto, como:

### RDP (Remote Desktop Protocol): Usado comúnmente para acceder a escritorios Windows.
### VNC (Virtual Network Computing): Protocolo para compartir escritorios de forma remota.
### SSH (Secure Shell): Usado para acceder a terminales de línea de comandos en sistemas basados en Unix/Linux.





###  Link Pagina Oficial:


https://github.com/flcontainers/guacamole



###  comando:

```yml
version: "3"
services:
  guacamole:
    image: flcontainers/guacamole
    container_name: guacamole
    environment:
      TZ: 'UTC'
      EXTENSIONS: 'auth-totp,auth-ldap'
    volumes:
      - postgres:/config
      - /etc/localtime:/etc/localtime:ro
    ports:
      - 8080:8080
volumes:
  postgres:
    driver: local
```


###  Claves de Acceso:

    Usuario: guacadmin

    Contraseña: guacadmin