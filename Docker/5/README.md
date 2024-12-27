# Mide la Velocidad de tu proveedor de Internet y valida que sea la correcta con SpeedTest.
## En Este Video Aprenderemos como validar que nuestro servicio de de internet sea el correcto validando nuestro servicio con SpeedTest.



###  Link Pagina Oficial:

https://docs.speedtest-tracker.dev/getting-started/installation/using-docker-compose


### paso 1 Aplicar este comando: 


    services:
        speedtest-tracker:
            image: lscr.io/linuxserver/speedtest-tracker:latest
            restart: unless-stopped
            container_name: speedtest-tracker
            ports:
                - 8080:80
                - 8443:443
            environment:
                - PUID=1000
                - PGID=1000
                - APP_KEY=
                - DB_CONNECTION=sqlite
            volumes:
                - /path/to/data:/config
                - /path/to-custom-ssl-keys:/config/keys



### Paso 2:

ir a este link y copiar la api Key:

    https://speedtest-tracker.dev/


### Paso 3:

Usuarios de acceso 

    Username

        admin@example.com

    Password
    
        password


No te Olvides de cambiar las credenciales de inicio por seguridad