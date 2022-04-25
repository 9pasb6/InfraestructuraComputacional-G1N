# TALLER USUARIOS Y PERMISOS

 
1. Se crean los grupos PROFESOR y ESTUDIANTE con el comando ***groupadd***.




![ccx](https://user-images.githubusercontent.com/100176897/165018138-99ae9db9-74df-4d44-916a-2979d84b9877.jpg)



-----

2. Se crean los usuarios Diana, Claudia y Laura con el comando ***useradd***.





------

    2a. Se les asignan contraseñas a dichos usuarios con el comando ***passwd***.





------

3. Se ubican los usuarios en sus respectivos grupos con el comando ***usermod*** y los argumentos ***-a*** y ***-G***.




-----

4. Se crean los directorios profesores y estudiantes 




-------

     4a. Nos aseguramos con el comando ***ls -la***.
 
 
 
 
 
 
 -------
 
 5. el usuario Laura (el cual pertenece al grupoestudiante) desea ingresar al directorio dirProfesores, el cual solo tiene acceso los que pertenecen al grupo profesor, por tal motivo se le niega el acceso.
 
 
 
 --------
     5a.En este caso podemos apreciar  como  el usuario claudia (profesor, estudiante) cuenta con los permisos de acceso para ambos directorios, el usuario diana (profesor), también cuenta con los permisos para ingresar a ambos directorios, por ultimo el usuario Laura (estudiante) solo cuenta con los permisos para acceder al directorio de estudiantes.
 
 
 
 ------
 
 6. Se crean archivos con diferentes usuarios en sus respectivos directorios.



--------
 7. Se cambian los dueños de los archivos contenidos en el directorio estudiante.


--------
    7a. se hace el mismo procedimiento en el directorio de profesores.



----------

8 y 9. Se realiza una prueba de errores para acceder a un usuario.



----------

10. Se accede al usuario y se verifica el numero de intentos fallidos con el comando ***lastb*** "nombreUsuario".


-------

11. Se comprime los contenidos del directorio de los profesores en profesore.tgz y
el contenido del directorio de los estudiante en un archivo estudiantes.zip



------------------------

12. Finalamente, se crea un alias para cambiar la clave del usuario diana 👩🏽.


 
 

> by Columbus 👽


