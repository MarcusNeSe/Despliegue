# Despliegue Practica de Máximo con Docker-Compose
___
**1 - Extraer .war del proyecto**
___
En nuestro caso como no hemos usado nuestro proyecto por falta de código y funcionamiento hemos cogido otro .war

___
**2 - Creación de la carpeta y archivos "DockerFile", "docker-compose.yml..."**
___
Primero hemos creado una carpeta llama "PracticaCompose" en la cual hemos metido los siguientes archivos. (Debe acabar algo parecido a esto menos con la carpeta "src")

![image](https://user-images.githubusercontent.com/101186662/173049920-b2e9411c-e39a-49c6-8d41-d9ccd574e7dd.png)

Una vez tengamos la carpeta lo que haremos será crear un archivo llamado "Dockerfile", nosotros lo hemos creado desde el visual. 

![image](https://user-images.githubusercontent.com/101186662/173050364-1aff1043-43d1-495b-803b-58a201650ac4.png)

Luego hay que poner la siguiente información. Por ejemplo en maintainer puedes cambiar el nombre por el tuyo.

Lo que hace el COPY es copiar el archivo llamado "LoginWebApp" que está situado en la carpeta "target", lo copiará en la siguiente ubicación "/usr/local/tomcat/webapps/".

![image](https://user-images.githubusercontent.com/101186662/173050465-1913228b-9aee-4a9e-ac64-13041d96a61e.png)

Ahora crearmos el archivo "docker-compose.yml", en el cual pondremos toda la información de cada contenedor como el de "mySql", "phpMyAdmin" y "tomcat". Lo hemos creado de la misma forma que el "Dockerfile", pero cambiando el nombre por "docker-compose.yml". En este archivo hemos puesto lo siguiente.

En el archivo .yml lo que escribimos son las versiones, indicamos que puerto queremos para cada contenedor, por ejemplo en la base de datos hemos elegido el puerto "3306", par el phpMyAdmin el puerto "8081" y para la web el puerto "8082". Todo esto si no lo haces sobre un servidor lo podrás visualizar de la siguiente forma (cuando este desplegado) "localhost:"puerto"" (ejemplo: localhost:8081 y visualizariamos el phpMyAdmin).

![image](https://user-images.githubusercontent.com/101186662/173051208-43f44d55-2b04-4a0b-af94-67455748cb98.png)
![image](https://user-images.githubusercontent.com/101186662/173051240-ae8bb703-f382-4b71-91b4-945286cf71af.png)

Ahora crearemos la carpeta "mysql-dump" y "target" estás dos carpeta cuando usamos el comando `docker-compose up -d` para levantar los tres contenedores a la vez se crean solas pero sin nada, menos la de "target" que lo que hace es crear otra carpeta dentro llamada "LoginWebApp.war" pero no necesitamos esa carpeta dentro sino el archivo "LoginWebApp.war".

En la carpeta "mysql-dump" crearemos el archivo "USUER.sql" con el siguiente contenido.

![image](https://user-images.githubusercontent.com/101186662/173052521-406d39eb-0657-4e3e-8aa2-5ea229140f99.png)

![image](https://user-images.githubusercontent.com/101186662/173052563-3ba676e5-be7f-4ed7-b72b-9464de0fcbad.png)
![image](https://user-images.githubusercontent.com/101186662/173052598-dbe31841-8d56-48c8-8c46-8d4a743b0df9.png)

En la carpeta "target" tendremos el archivo "LoginWebApp.war" y una carpeta "LoginWebApp" en esta carpeta tendremos todo el código. También tenemos el archivo "LoginWebApp.war.bck" que es una copia de seguridad del war.

![image](https://user-images.githubusercontent.com/101186662/173053095-dfa2ed4a-f62d-41b1-840f-f1c22f33b551.png)
