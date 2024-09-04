## DMIT API PROJECT - DOCKER
Éste repositorio dockeriza php 8.1 con MySql 8
En su carpeta src corre una versión de Laravel 10 con los componentes base para correr una Api rest.

## Renovación de Certificados

#### Debes parar los contenedores para esto

### www.dmit.ar

Para renovar los certificados SSL para el dominio www.dmit.ar, puedes utilizar el siguiente comando:

```bash
sudo certbot certonly --standalone --config-dir /home/dima/dmit-docker/ssl-certificates -d www.dmit.ar
```

Este comando utilizará Certbot para renovar los certificados SSL de manera independiente, sin necesidad de un servidor web en ejecución.

Recuerda reemplazar `/home/dima/dmit-docker/ssl-certificates` con la ruta correcta donde se encuentran los certificados en tu sistema.

Una vez ejecutado el comando, los nuevos certificados serán generados y almacenados en la ubicación especificada.

### Verificar vigencia del certificado 

```bash
openssl x509 -enddate -noout -in /home/dima/dmit-docker/ssl-certificates/live/www.dmit.ar/cert.pem
```


