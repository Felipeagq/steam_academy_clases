---
tags: cmd,bash,STEAM,clases
---
# Comandos CMD
# Clase 2
### Exploración y movimiento en la terminal.
- ````whiami````
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
- ````cat [file] [file] [file]```` : visualizar todo el archivo.
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

## PipeOperator
💡Los filtros son el procesos de tomar una entrada de flujo y, realizando una conversión, es mandado a la salida de otro stream.
Hace que la salida de uno sea la entrada de otro comando ````|````.
ejemplos:
- ````ls | grep <texto>````
- ````Command 1 | command 2 | command 3 ````
- ````ls -lh | sort | cat````

## Operadores de control
Son símbolos reservados por la terminal que nos permiten ejecutar varios comandos seguidos, e incluso agregar condicionales ⛓️.
- Síncronos: Se corre uno detrás de otro, en orden. Se hace esto con ````;```` , por ejemplo```` ls; mkdir carpeta1````
- Asíncrono: Por cada comando, se abre una nueva terminal, y cada comando se corre de manera paralela, esto es con ````&````, por ejemplo ````ls & date & mkdir carpeta```` ⏲️
- Condicionales: Podemos agregar lógica a como se corren los comandos:

    - AND: Si se cumple un comando, entonces se ejecuta el siguiente, se usa ````&&````, un ejemplo es ````mkdir carpeta1 && cd carpeta1 && echo "Si se pudo"```` . Si no se puede ejecutar el primer comando, no se ejecuta el siguiente. 🚆
    - OR: Se ejecuta el primer comando que se pueda ejecutar, y se usa ````||````, por ejemplo ````cd carpeta || echo "No hay carpeta"````, el comando siguiente funciona si el comando anterior da con error.


## Variables de entorno
- para ver las variables de entorno
````printenv````
- ````export HOLA="Hola chicos"````
- ````$HOLA````

### Crearlas
1. a la altura del usuario creamos el archivo ````cat > .bashrc````.
2. Ingresamos los alias ````alias [ALIAS]=[COMANDO]````
3. cargamos al sistema ````source .bashrc````
4. se creará por defecto un ````.bash_profile````


## Comandos de busqueda 

### Banderas del comando find
Banderas básicas:

- ````-name````: Realiza una búsqueda por nombre de archivo.
- ``-iname``: Realiza una búsqueda por nombre de archivo sin tomar en cuenta las mayúsculas o minúsculas.
- ``-type``: Realiza una búsqueda por tipo de archivo, f(files) y d(directories) que son los más comunes.
- ``-size``: Realiza una búsqueda por el tamaño de archivo y/o directorio.
Banderas de tiempo⏰

- ``-mmin``: Búsqueda por tiempo en minutos.
- ``-mtime``: Búsqueda por tiempo en días.
Más banderas👀

- ``-maxdepth``: Después de está bandera se pone el número de niveles de profundidad en los que queremos realizar la búsqueda
- ``-empty``: Realiza una búsqueda de archivos y/o directorios vacíos.
- ``-perm``: Búsqueda de archivos por permisos.
- ``-not``: Retorna los resultados que no coinciden con la búsqueda.
- ``-delete``: Está bandera se coloca al final del comando, eliminara los resultados de la busqueda(⚠️Hay que tener mucho cuidado al usarla).

Comandos de búsqueda

- Es una de las partes mas interesantes de la terminal, ya que nos permite buscar archivos de manera eficiente y específica 💫.
- which <programa> Busca en todas las rutas del PATH para encontrar donde está alojado algún archivo binario 🔢.
- find <ruta inicial> -name <archivo> Nos permite encontrar un archivo a partir de una ruta inicial, y dentro de todas las carpetas que surjan de ese inicio 🌲.
- Algo muy cool es que podemos usar wildcards para hacer mas eficiente la búsqueda 🔍.
- ``find <ruta inicial> -type <tipo> -name <nombre>`` podemos especificar el tipo de archivo, d → directorio, f → documento.
- ````find <ruta inicial> -size <tamaño><unidad> ````podemos buscar tamaños mayores a un determinado tamaño, por ejemplo, de 20M (megas).
- Solución al reto:```` find ./ -name *.txt -type f -size 1M > mis_archivos_texto.txt | echo "archivos guardadados exitosamente"````

### Ejemplos

````
Búsqueda de archivos vacíos a partir del directorio actual.
find . -type f -empty

Buscar todos los archivos de tipo directorio de profundidad 2
find ./ -maxdepth 2 -type d 

find ./ -maxdepth 2 -name *.txt

find ./ -maxdepth 2 -type d -name Doc*

````



## Premisos
|Atributo|	Tipo de archivo|
|--|--|
|-|	Es un archivo normal, como un documento de texto, una foto, un video, etc.
|d|	Por directory es un directorio
|l|	Es un enlace simbólico. Es algo que veremos en próximas clases
|b|	Bloque especial, son archivos que manejan información para el sistema, como la información de un disco duro

|Símbolo|Significado	|Permiso|
|--|--|--|
|r|	readable|	Significa que puede leer su contenido
|w|	writable|	El usuario puede editar el contenido del archivo, también el nombre y los permisos
|x|	executable|	El usuario puede ejecutarlo en caso de que sea un pr

![](./imagenes/permisos.png)
![](./imagenes/permisos_2.png)
![](./imagenes/permisos_3.png)
![](./imagenes/permisos4.png)
![](./imagenes/permisos5.png)

### Ejemplo
- ````chmod [PERMISOS] [FILE/DIRECTORY]````
- ````chmod [simboloDelUsuario][operador][permiso] [archivoParaCambiarSusPermisos]````
- ````chmod u-x,go=x [file]````