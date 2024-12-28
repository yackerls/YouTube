# Instalar Grafana para Crear Dashboard y Proyectar mis Estadísticas de mis Servidores.
### En este Video veran como se instala grafana y se corre y sus primeros pasos para la configuración de Dashboard de nuestras aplicaciones o servicios que tengamos corriendo.




###  Link Pagina Oficial:


https://grafana.com/docs/grafana/latest/setup-grafana/installation/docker/



###  comando:

```yml
services:
  grafana:
    image: grafana/grafana-enterprise
    container_name: grafana
    restart: unless-stopped
    ports:
      - '3000:3000'
    volumes:
      - grafana-storage:/var/lib/grafana
volumes:
  grafana-storage: {}
```


###  Claves de Acceso:

    Usuario: admin

    Contraseña: admin