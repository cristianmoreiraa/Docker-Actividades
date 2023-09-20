# <font color="red"> ***Docker - Comandos Básicos***  </font>

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


4. ültimo paso de este apartado, deberemos abrir la terminal y escribir: `ping google.com` y ya le abremos hecho ping a google.

## 5. Crea un contenedor con el nombre 'dam_ubu2'. ¿Puedes hacer ping entre los contenedores?

- Para crear el contenedor con el nombre **"dam_ubu2"**, debemos usar un comando que ya conocemos de pasos anteriores, `docker run -it --name dam_ubu2 ubuntu`

- Debemos instalar ping como hicimos en el paso 4. Y una vez que sabemos las 2 ip de cada contendor, podremos hacer ping mediante el comando `ping ip_contenedor`


## 6. Sal del terminal, ¿que ocurrió con el contenedor?

1. Para poder salir de la terminal simplemente podemos escribir `exit` y ya estaremos fuera de ella.
2. Una vez hecho el paso anterior, simplemente hemos cerrado la terminal no hemos borrado los contenedores, podremos volver a ellos con el comando `docker ps -a` y será fácil identificarlos, ya que tenemos los nombres de esos contenedores ***dam_ubu1*** y ***dam_ubu2***.
3. Si volvemos a abrir la terminal podemos comprobar con el comando `docker ps` y veriamos los contenedores que siguen activos.


## 7. ¿Cuanta memoria en el disco duro ocupaste?

Si queremos ver la memoria que ocupa un contenedor, podemos hacerlo de manera general con el comando `docker df`, si queremos verlo de manera más especifica usaremos el mismo comando añadiendole **-v**, quedaría así: `docker df -v`.

> En mi caso **dam_ubu1** ocupa un poco menos que el contenedor **dam_ubu2** (45.7) .

## 8. ¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto

