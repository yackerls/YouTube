# Crea tus propios certificados con Nginx Proxy Manager
### En este Video, verán como se instala Nginx y como se conecta con CloudFlare para generar tus propios certificados.




###  Link Pagina Oficial:


https://github.com/NginxProxyManager/nginx-proxy-manager



###  comando:

```yml
services:
  app:
    image: 'docker.io/jc21/nginx-proxy-manager:latest'
    restart: unless-stopped
    ports:
      - '80:80'
      - '81:81'
      - '443:443'
    volumes:
      - ./data:/data
      - ./letsencrypt:/etc/letsencrypt
```


###  Claves de Acceso:

http://0.0.0.0:81


    Usuario: admin@example.com

    Contraseña: changeme