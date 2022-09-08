---
tags: cmd,bash,STEAM,clases
---
# Comandos CMD
# Clase 2
### Exploración y movimiento en la terminal.
-  ````ls````
-  ````ls -R```` : busqueda recursiva de archivos.
-  ````rm -rf [directory]```` : eliminar de forma "recursiva" y "force".
-  ````rm -i [file]```` : eliminar de forma interactiva.
-  ````pwd```` : print work directory
-  ````mkdir [directorio]````
-  ````cd```` : change directory.
-  ````file [archivo]```` : identificar el tipo y formato de un archivo.
-  Tree:

### Tree

```sudo apt install tree```

- ````tree````        # Muestra directorios y ficheros

- ````tree -d````     # Muestra sólo directorios

- ````tree -L X````   # Muestra hasta X directorios de profundidad

- ````tree -f````     # Muestra los archivos con su respectiva ruta

- ````tree -a````     # Muestra todos los archivos, incluidos los ocultos.

- ````tree /````      # Muestra un árbol de todo nuestro sistema

- ````tree -ugh````   # Muestra los ficheros con su respectivo propietario (-u),
el grupo (-g) y el tamaño de cada archivo (-h)

- ````tree -H . -o tudirectorio.html```` # Exporta tu árbol de directorio a un archivo
HTML


### manipular archivos
- ````touch```` : crea un archivo en blanco, solo lo "toca".
- ````cp [origen] [destino]```` : copiar archivos.
- ````mv [origin] [destino]```` : mover un archivo, tambien puede renombrar los archivos.
- ````head [file] -n [lineas]```` : muestras las primeras [lineas] de un archivo.
- ````cat [file]```` : visualizar todo el archivo.
- ````tail [file] -n [lineas]```` : muestra las ultimas [lineas] de un archivo.
- ````less [file]```` : ver el contenido de un archivo de forma interactiva, se sale con la "q", nos permite buscar un con ````/[palabra]````.
- ````explorer.exe .```` : para abrir el explorador grafico de archivos.

### Explorar comandos
- ````type [comando]```` : ver que tipo de comandos es.
- ````alias [alias]="script del comando"```` : crear un nombre para un comando.
- ````whatis [comando]```` : dice una breve descripción de los que es el comando.
- comando man: ayuda interactiva de comandos y tecnologias.
```
sudo apt update
sudo apt install man-db manpages-posix
man [comando]
```


## Imagenes
-  ![](http://localhost:10001/uploads/54c07e6e-0482-47cd-a044-59e60f7e1576.png)
-  ![](http://localhost:10001/uploads/9149f1bb-26aa-4376-99f2-536ea0b334c5.png)
-  ![](http://localhost:10001/uploads/f0b45953-baad-46be-953f-f1e8f0182166.png)
-  -  ![](http://localhost:10001/uploads/e7fb77ae-1fdb-4f35-9408-18e10944b9ed.png)

## **Comando "Start" en windows:**
    - https://norfipc.com/comandos/como-usar-comando-start-windows-aplicaciones-practicas.php
    - https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/start
    - https://www.colorconsole.de/console/es/062.htm
    

## Wildcards
- Son una serie de caracteres especiales que nos permiten realizar búsquedas muy avanzadas utilizando ls 🔍. Puedes utilizar wildcards con otros comandos que realicen manipulación de archivos como mv, cp o rm 💫. También se conocen como comodines.
- ls ````<texto>````: Nos muestra todos los archivos que tengan en su nombre dicho texto al final. Si haces ls ````<texto>*```` lo busca al final. El asterisco significa cualquier string.
- ls ````<text>?```` El signo de interrogación sustituye a cualquier carácter, por ejemplo, buscamos todos los archivos que tengan una palabra y un número dado de caracteres después. El signo de interrogación significa cualquier carácter.
- ```ls [[:upper:]]*``` Para filtrar cosas que inicien que una mayúscula; esto busca también dentro de los directorios.
- ```ls [[:lower:]]*``` Lo mismo pero con minúsculas.
- ```ls -d``` Se muestran solo directorios.
- ```ls [ad]*``` Todo lo que inicie con a o con b
- ```ls *.txt```: Lo que hace este comando es listar todos los archivos que tengan extensión .txt, independientemente del nombre que tengan.
- ```ls datos*```: Lo que hace este comando es listar todos los archivos que inicien con la palabra “datos”, independientemente de cómo siga el nombre o la extensión que tenga.
- ```ls datos?```: Lo que hace este comando es listar todos los archivos que inicien con la palabra “datos” y solamente tengan un caracter más luego de esa palabra.
- ```ls datos???```: Lo que hace este comando es listar todos los archivos que inicien con la palabra “datos” y solamente tengan tres caracteres más luego de esa palabra.
- ```ls [[:upper:]]*```: Lo que hace este comando es listar todos los archivos que inicien con una mayúscula, independientemente de cómo siga el nombre o la extensión que tenga.
- ```ls -d [[:upper:]]*```: Lo que hace este comando es listar todos los DIRECTORIOS que inicien con una mayúscula, independientemente de cómo siga el nombre que tenga.
- ```ls [[:lower:]]*```: Lo que hace este comando es listar todos los DIRECTORIOS que inicien con una minúscula, independientemente de cómo siga el nombre o la extensión que tenga.
- ```ls [ad]*```: Lo que hace este comando es listar todos los archivos que inicien con la letra “a” o con la letra “d”, independientemente de cómo siga el nombre o la extensión que tenga.
    
##  Redirecciones: Cómo funciona la shell.
    
- Normalmente, cuando pones un comando en la terminal, la salida se muestra ahí mismo, pero se puede redirigir la salida a un archivo 👀. Si la salida es correcta tiene file descriptor 1, si no, file descriptor 2.
- La entrada estándar es nuestro teclado que tiene file descriptor 0, pero también puede venir de otro lado 🧠.
- Para redirigir algo usamos >. Por ejemplo ```ls > misarchivos.txt```, entonces la salida del comando se guarda en ese archivo de texto. Siempre crea este archivo (si ya existe, lo reescribe).✍🏽
- Para que se concatene la salida en un archivo preexistente usa ```"comando" >> "archivo"```. Esto ambos solo redirigen los stdout.
- Para redirigir stderr, agregas su file descriptor ```"comando" 2> "archivo"```. 👽
- Si quiere redirigir cualquiera de las dos opciones ```"comando" >> "archivo" 2>&1```.
- Esto nos puede servir para, por ejemplo, guardar los mensajes de error que manda un servidor 🤯.
- Para redirigir stdin se usa ```<```. Esto te permite tener de entrada de comandos algún archivo.