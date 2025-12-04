# Práctica de clase

<br>

## Pasos seguidos

<br>

Dentro del directorio ``.github/workflows`` he creado el archivo ``docker-image.yml`` para generar laiamgen y publicarla en Docker Hub:

### PASO 1:

Me ubico en la rama desde la que quiero que se genere el actions: 

https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/8abea3abdd35641bd46fdfc0b8333dff751237ad/.github/workflows/docker-image.yml#L3-L7

## PASO 2:

Configuro sobre qué versión voy a ejecutar el actions, en este caso la última versión de Ubuntu:

https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/8abea3abdd35641bd46fdfc0b8333dff751237ad/.github/workflows/docker-image.yml#L13

## PASO 3:



https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/8abea3abdd35641bd46fdfc0b8333dff751237ad/.github/workflows/docker-image.yml#L16-L17

## PASO 4:

Primero, inicio sesión en mi cuenta de DockerHub en el navegador para generar el token de acceso necesario. Luego, me he dirigido a la configuración del repositorio para añadir dos secretos nuevos: ``DOCKER_USERNAME`` con mi nombre de usuario de DockerHub y ``DOCKER_PASSWORD`` donde he colocado el token que he generado.

He usado el action ``docker/login-action`` para iniciar sesión, usando los dos secretos que he añadido en el repositorio.

https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/8abea3abdd35641bd46fdfc0b8333dff751237ad/.github/workflows/docker-image.yml#L19-L23

## PASO 5:

En este paso, construyo la imagen con los comandos de docker y empleando el nombre de la imagen que he encontrado en el archivo ``docker-compose.yml`` junto a la versión ``lastest``: springboot-crud-app 

https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/8abea3abdd35641bd46fdfc0b8333dff751237ad/.github/workflows/docker-image.yml#L25-L28
