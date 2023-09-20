# ***Docker - Comandos Básicos***

<br>

## 1. Descarga la imagen de Ubuntu y comprueba que está en tu equipo:

`docker run ubuntu` 

        Este comando nos permite descargar la imagen de manera local.
`docker imagen ls -a`

        Este comando nos permite ver las imagenes que ya tenemos instaladas.


## 2. Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre

- Para crear un contenedor sin nombre utilizaremos el comando: `docker run ubuntu`
- A continuación con el comando: `docker ps -a` Nos permite mirar los contenedores que tenemos creados, pero aun así estarán de manera "apagada". El contenedor que acabo de crear se hizo con el nombre de *"lucid_lederberg"*.

<details><summary>Ver la tabla con la información:</summary>

|CONTAINER ID|IMAGE|COMMAND|CREATED|STATUS|PORTS|NAMES|
|------|------|------|------|------|------|------|
|8b4cb45a7762|ubuntu|"/bin/bash" |5 seconds ago|Exited (0) 4 minutes ago||lucid_lederberg|

</details>


