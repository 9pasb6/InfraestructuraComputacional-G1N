 
# Docker Desktop 馃惓

Se emplear谩n unas cuantas funcionalidades de Docker Desktop que nos podr谩 ayudar a correr nuestros contenedores y administrar nuestras im谩genes. 

A continuaci贸n, un ejemplo de c贸mo contener una aplicaci贸n en java.

Paso 1: crear nuestro c贸digo o aplicaci贸n en java, para poder realizar dicho c贸digo se puede emplear la herramienta Spring Boot, donde para esta demostraci贸n utilizaremos Maven, la versi贸n de java que deseemos, definimos la forma del paquete y por ultimo la dependencia, que en este caso ser谩 una dependencia web, luego damos al bot贸n de generar.

Paso 2: abrir visual studio code, para visualizar el c贸digo descargado de Spring Boot, con el prop贸sito de poder administrar las dependencias, una vez all铆, importamos RequestMappin y RestController, para poder construir un m茅todo que nos responda por la url principal del api y nos responda con un mensaje 鈥渉ello Word鈥?.

Nota: asegurarse de tener Maven y java instalado en nuestro ordenador, este 煤ltimo con una versi贸n posterior a la 17 

### COMPILAR CODIGO

Generamos nuestro jar con el comando ./mvnw package, luego miramos en el target para verificar la creaci贸n de este, posteriormente leemos el Dockerfile-build, donde enviamos un argumento que el jar de la carptea target, donde lo que hace es copiar  el jar al contenedor y ejecutar la instrucci贸n ENTRYPOINT.

A  continuaci贸n ejecutamos el comando java -jar target/spring-boot-docker-0.0.1-SNAPSHOT.jar donde este empieza a  iniciar una aplicaci贸n en springboot.
Para saber por cual puerto se inicia debemos mirar en el Tomcat started on ports: ###, con el prop贸sito de verificar de que es el servicio correcto y que est谩 funcionando.

-----------
### CREAR UNA IMAGEN

Creamos una imagen a trav茅s del DockerFile, con el comando Docker build -f Dockerfile-build -t nombreImagen .
Con esto empezar谩 a construir la imagen, para verificar la existencia de esta imagen empleamos el comando Docker image ls , luego ejecutamos la imagen creada en un contenedor a trav茅s del comando
Docker run -p 8080:8080 -t spring-boot con esto estamos ejecutando spring desde el contenedor, con el comando Docker container ls podemos ver que se esta ejecutando un contenedor.

-----------

### ABRIR DOCKER

En Docker podemos visualizar, sus variables de entorno, donde se encuentra java, sus argumentos y el comando que va ha ejecutar, donde podemos ejecutar un contenedor y ponerle el nombre que deseemos, como: mi_primer_contenedor_spring_boot y definir los puertos y vol煤menes.

Ahora, el contenedor que esta ejecutando nuestra imagen spring boot, nos permite ver que se esta ejecutando, donde podemos ir al navegador y ejecutar localhost 8080, el va a responder desde el contenedor con el 鈥渉ello Word鈥?, donde podemos ver todo tipo de elementos que tiene nuestro contenedor, como sus estad铆sticas; adem谩s podemos detener nuestro contenedor, donde nos va a indicar que no puede responder, en caso contrario la aplicaci贸n va a responder, podemos reiniciar el contenedor en caso de falla, por ultimo podemos eliminar nuestro contenedor.


Bibliograf铆a:

https://www.youtube.com/watch?v=WlvxqJVn7OU   馃鈥嶐煉?

https://www.docker.com/blog/kickstart-your-spring-boot-application-development/

> by Columbus 馃懡

