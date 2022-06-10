# Despliegue Practica de Máximo con Docker-Compose
___
**1 - Extraer .war del proyecto**
___
En nuestro caso como no hemos usado nuestro proyecto por falta de código y funcionamiento hemos cogido otro .war

___
**2 - Creación de la carpeta y archivos "DockerFile", "docker-compose.yml..."**
___
Primero hemos creado una carpeta llama "PracticaCompose" en la cual hemos metido los siguientes archivos. (Debe acabar algo parecido a esto)

![image](https://user-images.githubusercontent.com/101186662/173049920-b2e9411c-e39a-49c6-8d41-d9ccd574e7dd.png)

Una vez tengamos la carpeta lo que haremos será crear un archivo llamado "Dockerfile", nosotros lo hemos creado desde el visual. 

![image](https://user-images.githubusercontent.com/101186662/173050364-1aff1043-43d1-495b-803b-58a201650ac4.png)

Luego hay que poner la siguiente información. Por ejemplo en maintainer puedes cambiar el nombre por el tuyo.

Lo que hace el COPY es copiar el archivo llamado "LoginWebApp" que está situado en la carpeta "target", lo copiará en la siguiente ubicación "/usr/local/tomcat/webapps/".

![image](https://user-images.githubusercontent.com/101186662/173050465-1913228b-9aee-4a9e-ac64-13041d96a61e.png)

Ahora crearmos el archivo "docker-compose.yml", en el cual pondremos toda la información de cada contenedor como el de "mySql", "phpMyAdmin" y "tomcat". Lo hemos creado de la misma forma que el "Dockerfile", pero cambiando el nombre por "docker-compose.yml". En este archivo hemos puesto lo siguiente.

