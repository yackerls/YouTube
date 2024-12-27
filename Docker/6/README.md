# Base de datos para tus aplicaciones InfluxDB
## En este video veremos como Instalar InfluxDB que nos ayudara con las gestión de nuestras bases de datos.

¿Qué es InfluxDB?
InfluxDB es un sistema de gestión de bases de datos desarrollado por la empresa InfluxData, Inc



###  Link Pagina Oficial:


https://hub.docker.com/_/influxdb


###  comando 1:

    docker pull influxdb




###  comando 2:


    docker run \
        -p 8086:8086 \
        -v "$PWD/data:/var/lib/influxdb2" \
        -v "$PWD/config:/etc/influxdb2" \
        influxdb:2
