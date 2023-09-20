# <font color="red""> ***Docker - Comandos Básicos*** </font>

###### Antes de nada camibaremos de la rama **MASTER** a la rama **MAIN**, mediante el comando `git branch -M main`.


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


## 3. Crea un contenedor con el nombre 'dam_ubu1'. ¿Como puedes acceder a él?
        
*   En este paso 3, el comando que necesitaremos usar será: `docker run -it --name dam_ubu1 ubuntu` Este comando, nos permite crear el contenedor con el nombre que queremos, además el la parte del código `-it` nos deja poder interacturar con el.

## 4. Comprueba que ip tiene y si puedes hacer un ping a google.com

1. Antes de comprobar la ip de nuestro equipo debemos descargar **net-tools**, mediante el comando:

    `apt update`
        
        Este comando nos actualiza los paquetes

    `apt install net-tools`

        Nos descarga el paquete de net-tools
2. Ahora ya podemos comprobar la ip de nuestro ordenador usando `ipfconfig`.
3. En tercer lugar para poder hacer ping a google, debemos instalar el paquete **iputils-ping**.

    `apt install iputils-ping`

        Descarga el paquete y ya podrémos hacer ping    



