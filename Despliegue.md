# Práctica de clase

<br>

## Pasos seguidos

<br>

Dentro del directorio ``.github/workflows`` he creado el archivo ``docker-image.yml`` para generar laiamgen y publicarla en Docker Hub:

### PASO 1:

Me ubico en la rama desde la que quiero que se genere el actions: 

https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/8abea3abdd35641bd46fdfc0b8333dff751237ad/.github/workflows/docker-image.yml#L3-L7

### PASO 2:

Configuro sobre qué versión voy a ejecutar el actions, en este caso la última versión de Ubuntu:

https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/8abea3abdd35641bd46fdfc0b8333dff751237ad/.github/workflows/docker-image.yml#L13

### PASO 3:

Empleo un actions para comprobar el estado del repositorio:

https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/8abea3abdd35641bd46fdfc0b8333dff751237ad/.github/workflows/docker-image.yml#L16-L17

### PASO 4:

Primero, inicio sesión en mi cuenta de DockerHub en el navegador para generar el token de acceso necesario. Luego, me he dirigido a la configuración del repositorio para añadir dos secretos nuevos: ``DOCKER_USERNAME`` con mi nombre de usuario de DockerHub y ``DOCKER_PASSWORD`` donde he colocado el token que he generado.

He usado el action ``docker/login-action`` para iniciar sesión, usando los dos secretos que he añadido en el repositorio.

https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/8abea3abdd35641bd46fdfc0b8333dff751237ad/.github/workflows/docker-image.yml#L19-L23

### PASO 5:

En este paso, construyo la imagen con los comandos de docker y empleando el nombre de la imagen que he encontrado en el archivo ``docker-compose.yml`` junto a la versión ``lastest``: ``springboot-crud-app``. 

https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/8abea3abdd35641bd46fdfc0b8333dff751237ad/.github/workflows/docker-image.yml#L25-L28

### PASO 6:

Subo la imagen a DockerHub

https://github.com/Lmrocio/2526_DAW_u2_springboot/blob/88fcb477e87e15e809a00541bdb926d54cedad3e/.github/workflows/docker-image.yml#L30-L31

### PASO 7:

He hecho un commit de prueba y compruebo que el actions se completa correctamente:

<img width="918" height="661" alt="Captura de pantalla 2025-12-04 101906" src="https://github.com/user-attachments/assets/795bd1eb-7539-4634-811d-7c8a71899cf3" />


### PASO 8:
He comprobado desde mi cuenta de DockerHub que la imagen se ha subido:

<img width="1284" height="277" alt="Captura de pantalla 2025-12-04 101213" src="https://github.com/user-attachments/assets/244bd9cc-fa60-47d1-92a9-a63c1546e03e" />

### PASO 9:

He realizado cambios en el HTML de la app para colocar mi nombre en el título, junto a 'Gestor usuario:'.

### PASO 10:

En la terminal del IDE ejecuto el comando ``docker compose up -d`` para levantar la app. Compruebo en ``localhost:8080`` y no veo los cambios que he generado en el HTML, pero al probar desde la terminal de DockerDesktop a descargar la imagen desde mi cuenta de DockerHub, he comprobado que funciona.

<img width="1909" height="1027" alt="Captura de pantalla 2025-12-04 102459" src="https://github.com/user-attachments/assets/5ab671fa-3865-48a1-86df-0c0e1198bc9b" />

