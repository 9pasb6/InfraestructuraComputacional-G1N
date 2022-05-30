 
##Docker Desktop##

Se emplearán unas cuantas funcionalidades de Docker Desktop que nos podrá ayudar a correr nuestros contenedores y administrar nuestras imágenes. 

A continuación, un ejemplo de cómo contener una aplicación en java.

Paso 1: crear nuestro código o aplicación en java, para poder realizar dicho código se puede emplear la herramienta Spring Boot, donde para esta demostración utilizaremos Maven, la versión de java que deseemos, definimos la forma del paquete y por ultimo la dependencia, que en este caso será una dependencia web, luego damos al botón de generar.

Paso 2: abrir visual studio code, para visualizar el código descargado de Spring Boot, con el propósito de poder administrar las dependencias, una vez allí, importamos RequestMappin y RestController, para poder construir un método que nos responda por la url principal del api y nos responda con un mensaje “hello Word”.

Nota: asegurarse de tener Maven y java instalado en nuestro ordenador, este último con una versión posterior a la 17 

COMPILAR CODIGO

Generamos nuestro jar con el comando ./mvnw package, luego miramos en el target para verificar la creación de este, posteriormente leemos el Dockerfile-build, donde enviamos un argumento que el jar de la carptea target, donde lo que hace es copiar  el jar al contenedor y ejecutar la instrucción ENTRYPOINT.

A  continuación ejecutamos el comando java -jar target/spring-boot-docker-0.0.1-SNAPSHOT.jar donde este empieza a  iniciar una aplicación en springboot.
Para saber por cual puerto se inicia debemos mirar en el Tomcat started on ports: ###, con el propósito de verificar de que es el servicio correcto y que está funcionando.

CREAR UNA IMAGEN
Creamos una imagen a través del DockerFile, con el comando Docker build -f Dockerfile-build -t nombreImagen .
Con esto empezará a construir la imagen, para verificar la existencia de esta imagen empleamos el comando Docker image ls , luego ejecutamos la imagen creada en un contenedor a través del comando
Docker run -p 8080:8080 -t spring-boot con esto estamos ejecutando spring desde el contenedor, con el comando Docker container ls podemos ver que se esta ejecutando un contenedor.

ABRIR DOCKER

En Docker podemos visualizar, sus variables de entorno, donde se encuentra java, sus argumentos y el comando que va ha ejecutar, donde podemos ejecutar un contenedor y ponerle el nombre que deseemos, como: mi_primer_contenedor_spring_boot y definir los puertos y volúmenes.

Ahora, el contenedor que esta ejecutando nuestra imagen spring boot, nos permite ver que se esta ejecutando, donde podemos ir al navegador y ejecutar localhost 8080, el va a responder desde el contenedor con el “hello Word”, donde podemos ver todo tipo de elementos que tiene nuestro contenedor, como sus estadísticas; además podemos detener nuestro contenedor, donde nos va a indicar que no puede responder, en caso contrario la aplicación va a responder, podemos reiniciar el contenedor en caso de falla, por ultimo podemos eliminar nuestro contenedor.


Bibliografía:
https://www.youtube.com/watch?v=WlvxqJVn7OU

https://www.docker.com/blog/kickstart-your-spring-boot-application-development/

