# Despliegue Practica de Máximo con Docker-Compose
___
**1 - Extraer .war del proyecto**
___
En nuestro caso como no hemos usado nuestro proyecto por falta de código y funcionamiento hemos cogido otro .war

___
**2 - Creación de la carpeta y archivos "DockerFile", "docker-compose.yml..."**
___
Ahora lo que realizaremos será crear una carpeta con el nombre que queramos, dentro de el pondremos nuestro archivo .war.

![image](https://user-images.githubusercontent.com/101186662/172940806-f31dd053-9145-474f-aa64-d2c46374ff5c.png)

![image](https://user-images.githubusercontent.com/101186662/172940848-a9379084-82e0-4226-94c4-28aeeb51d3e0.png)

Seguido de esto vamos a crear un archivo llamado "DockerFile", dentro de dicho archivo colocaremos lo siguiente. En "LABLE" ponemos nuestro nombre. En "COPY" primero pondremos la ruta donde se encuentra nuestro archivo .war.

![image](https://user-images.githubusercontent.com/101186662/172940580-e54d868f-8394-478a-91fd-38841ca4b362.png)

Una vez tengamos el DockerFile terminado daremos click derecho y `Build Image...`

![image](https://user-images.githubusercontent.com/101186662/172942682-af24457b-8d57-45d2-884b-5e6f552dd77b.png)

![image](https://user-images.githubusercontent.com/101186662/172942696-d9a7f1bb-76ab-4636-a7ee-8d7d631578df.png)

Ahora crearemos el archivo `docker-compose.yml` en el cual pondremos lo siguiente. Como podemos ver hemos asignado el puerto "8081" para el tomcat.

![image](https://user-images.githubusercontent.com/101186662/172942882-4a0abe6c-04b4-4b00-873a-2e12f2daaac0.png)

Una vez tengamos hecho el `docker-compose.yml`, daremos click derecho y `Compose Up`, que sería lo mimso que ir a la terminal y ejecutar el comando `docker-compose up -d`.

![image](https://user-images.githubusercontent.com/101186662/172944035-33eb6fd4-6b95-4d95-80ac-79ecb59b42ba.png)

![image](https://user-images.githubusercontent.com/101186662/172944051-b0a0232a-90f2-49be-ad91-675170a2d3c8.png)

___
**3 - Visualiación de página (Login y Register)**
___
Ahora si ponemos en el navegador `localhost:8081/LoginWebApp/` y todo ha salido correctamente visualizaremos el login.

![image](https://user-images.githubusercontent.com/101186662/172944339-2f5ab794-7ddc-4c3d-95ea-87af9aa6d46a.png)

___
**4 - Push a GitHub**
___
Primero deberemos hacer un `docker login` e inciar sesión en docker para poder realizar un push y que se suba a nuestro perfil de docker hub. Nosotros lo hemos hecho desde Visual Studio ya que con tan solo darle a un botón y escribir el nombre que le queremos poner ya lo hará solo.

![image](https://user-images.githubusercontent.com/101186662/172944772-39795997-c8ab-42cd-9e5d-0786520dc7e5.png)

![image](https://user-images.githubusercontent.com/101186662/172944787-73c85b42-a17f-420a-89f7-bc91374ceb0d.png)

![image](https://user-images.githubusercontent.com/101186662/172944806-509c7a12-2dfc-46ca-8a30-6319b75ad573.png)

![image](https://user-images.githubusercontent.com/101186662/172944817-ec116d0c-e7d7-4673-94ff-dbe110363327.png)

Este es el enlace donde podemos hacer el pull[https://hub.docker.com/r/iglesiascarlos/practicacompose]

El primer paso que tenemos que hacer es exportar el proyecto en un fichero.war y lo guardaremos en una nueva carpeta. Para ello, desde Eclipse hacemos click derecho sobre el proyecto y lo exportamos como un archivo "WAR".
