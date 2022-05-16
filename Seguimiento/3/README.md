# TALLER USUARIOS Y PERMISOS

 
1. Se crean los grupos PROFESOR y ESTUDIANTE con el comando ***groupadd***.




![ccx](https://user-images.githubusercontent.com/100176897/165018138-99ae9db9-74df-4d44-916a-2979d84b9877.jpg)



-----

2. Con el comando ***useradd*** se crean los usuarios: 

     * Diana 👩🏿
     * Claudia 👩🏽
     * Laura 👩🏼‍🦱


![xc](https://user-images.githubusercontent.com/100176897/165021762-5e63bcbe-92df-48a8-a700-b49eeee7b81f.jpg)





------

    2a. Se les asignan contraseñas a dichos usuarios con el comando ***passwd***.

![2a](https://user-images.githubusercontent.com/100176897/165021820-c100ad62-f8ca-42a7-a07c-116565738624.jpg)




------

3. Se ubican los usuarios en sus respectivos grupos con el comando ***usermod*** y los argumentos ***-a*** y ***-G***.

![3 permisos](https://user-images.githubusercontent.com/100176897/165021888-ea18c52b-4ed3-4428-abde-0a6bbbc4a953.jpg)



-----

4. Se crean los directorios profesores y estudiantes 


![4 permisos](https://user-images.githubusercontent.com/100176897/165021956-30d791c6-a152-48ed-9138-3073816c8b1b.jpeg)

 
 
 
 
 
 
 -------
 
 5. el usuario Laura 👩🏼‍🦱(el cual pertenece al grupoestudiante) desea ingresar al directorio dirProfesores, el cual solo tiene acceso los que pertenecen al grupo profesor, por tal motivo se le niega el acceso.
 
 
 ![5](https://user-images.githubusercontent.com/100176897/165022082-2a9363af-969a-4bc1-aafd-0f5d09f3a199.jpeg)
 
 
 --------
 
   5a.En este caso podemos apreciar  como  el usuario claudia 👩🏽 (profesor, estudiante) cuenta con los permisos de acceso para ambos directorios, el usuario diana 👩🏿 (profesor), también cuenta con los permisos para ingresar a ambos directorios, por ultimo el usuario Laura 👩🏼‍🦱(estudiante) solo cuenta con los permisos para acceder al directorio de estudiantes.
     
 ![5a](https://user-images.githubusercontent.com/100176897/165022125-f08d47fd-a2ec-4431-ba5e-cda92e23ab0e.jpeg)

 
 
 
 ------
 
 6. Se crean archivos con diferentes usuarios en sus respectivos directorios.

![6 permisos](https://user-images.githubusercontent.com/100176897/165022190-3b86ea77-181f-4f8a-affb-b6a0987f549b.jpeg)


--------

 7. Se cambian los dueños de los archivos contenidos en el directorio estudiante.

![7 permisos](https://user-images.githubusercontent.com/100176897/165022263-5a7c48ba-3422-4dc2-866c-c8ead4ca7a21.jpeg)


--------

    7a. se hace el mismo procedimiento en el directorio de profesores.
    
![7a permisos](https://user-images.githubusercontent.com/100176897/165022301-2c62c8ff-3f2e-427b-bcfd-6ecad3e80840.jpeg)



----------

8 y 9. Se realiza una prueba de errores para acceder a un usuario.

![8 y 9 permisos](https://user-images.githubusercontent.com/100176897/165022368-9f792b2e-cb9b-49fd-912a-e2f012a3d967.jpeg)


----------

10. Se accede al usuario y se verifica el numero de intentos fallidos con el comando ***lastb*** "nombreUsuario".

![10 permisos](https://user-images.githubusercontent.com/100176897/165022400-688d19ed-d726-4d96-bc3e-be0c2629e5d0.jpeg)

-------

11. Se comprime los contenidos del directorio de los profesores en profesore.tgz y
el contenido del directorio de los estudiante en un archivo estudiantes.zip

![11 permisos](https://user-images.githubusercontent.com/100176897/165022446-bc69bef0-7685-423d-bbe9-81efaf8df2da.jpeg)


------------------------

12. Finalamente, se crea un alias para cambiar la clave del usuario diana 👩🏿.


 ![12 permisos](https://user-images.githubusercontent.com/100176897/165022491-0f407944-f679-49da-9121-1e8161186ee7.jpeg)

 

> by Columbus 👽


