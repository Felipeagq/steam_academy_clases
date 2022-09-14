
# Introducción al internet
# Clase 1
## Historia de la computación.
![](./imagenes_1/historia.png)
![](./imagenes_1/historia2.png)
![](imagenes_1/in_out.png)

🔹 La entrada o input son la información que ingresamos a la computadora, esto puede ser a través de dispositivos de entrada como: Escaner, Micrófono, WebCam, Mouse, Teclado, etc.

🔹 El Proceso consiste en los cálculos que hará la computadora tomando como base la informacion ingresada.

🔹 La salida o output son la información que devuelve la computadora y esta inforamción puede ser visualizada a través de dispositivos de salida como: Impresora, Proyector, Parlante, Monitor, etc.

## Lenguaje Binario
La base de los procesos anteriores es el lenguaje binario.
![](imagenes_1/binario.png)
### Ejercicio:
Convertir un numero decimal en binario.

## Bits y Bytes
![](./imagenes_1/bitd.png)
![](./imagenes_1/byte.png)
![](./imagenes_1/escala_byte.png)

## Codigo ASCII
https://www.ascii-code.com

El codigo ASCII es la representación simbolica de un numero decimal representado por un numero contruido en Bytes.
![](imagenes_1/ascci1.png)
![](./imagenes_1/ascii2.png)
### Ejercicios
- Convertir un texto a un codigo ASCII
- luego convertirlo en codigo binario.
- Calcular su peso en Bytes.
- Calcular su peso en Bits

## Unicode
- https://unicode-table.com/es/
- https://www.oscarlijo.com/blog/tabla-de-caracteres-unicode/
Unicode es un estándar de codificación de caracteres diseñado para facilitar el tratamiento informático, transmisión y visualización de textos de numerosos idiomas y disciplinas técnicas, además de textos clásicos de lenguas muertas. El término Unicode proviene de los tres objetivos perseguidos: universalidad, uniformidad y unicidad.
En caracter de unicode puede formarse desde 1 byte hasta 6 bytes.
![](imagenes_1/unicode.png)

## RBG
Es un formato de colores, donde cada pixel dentro de una imagen está compuesta por 3 subpixeles: Rojo (Red), Verde (Green) y Azul (Blue) con un tono de 0 a 255.
Ejemplos:
🔹 Negro (0, 0, 0)
🔹 Blanco (255, 255, 255)
🔹 Rojo (255, 0, 0)
⠀
Combinando tonalidades se pueden formar colores específicos.
⠀
Ejemplos:
🔹 Plum Purple (178, 80, 228) - 10110010, 01010000, 11100100


````info
**Porque verde? Si no es un color primario…**
Los pigmentos (pinturas) son colores de «sustracción». Ya sabes, el color que ves es el que no han absorbido de la luz. Al juntar azul y amarillo «absorben más frecuencias» y da el verde (modelo RYB, de las siglas de red, yellow y blue). Pero la luz es un modelo de adición: al juntar dos colores ves la suma de sus «frecuencias», es decir Verde + azul= amarillo (modelo RGB)
Por eso la TV y el PC usan modelos de RGB (emiten luz) pero el cartucho de tinta de tu impresora usa el RYB.

Cada pixel representa un cálculo de la computadora.
````
![](imagenes_1/rgb1.png)
![](imagenes_1/rgb2.png)

### Hexadecimal
Otro formato de colores es el Hexadecimal donde el RGB formado por 3 bytes, es traducido a Hexadecimal
![](imagenes_1/hexadecimal.png)

## Internet
https://www.submarinecablemap.com
![](imagenes_1/internet1.png)
![](imagenes_1/internet2.png)
![](imagenes_1/internet3.png)

## Protocolos
TCP (Tranmission Control Protocol) e IP (Internet Protocol) son los principales, sin protocolos de transmisión de cómo debe pasar la información. Se estructura en 5 etapas
- Aplicación: HTTP/ FTP
- Transporte: TCP/ UDP
- Red: IP/ Routers
- Enlace: Ethernet / Switchers
- Física: cables
  
![](imagenes_1/protocolos1.png)

![](imagenes_1/protocolos2.png)

![](imagenes_1/protocolos3.png)

![](imagenes_1/protocolos4.png)

![](imagenes_1/protocolos5.png)

## ISP
Un ISP o Proveedor de Servicios de Internet ( Internet Service Provider), es el término con el que se identifica a las compañías que proporcionan acceso a Internet, a los hogares… a empresas,etc

Es decir, puedes tener el ordenador más potente del mundo con una flamante tarjeta de red y la casa u oficina cableada con fibra óptica, que sin un ISP no tendrás la posibilidad de navegar. Y para poder navegar, es necesario pagar una cuota a uno de estos proveedores.Muchas veces nos estafan.
**¿CÓMO FUNCIONA UN ISP?**
Básicamente, lo que hace un ISP es desplegar una red de telecomunicaciones que se conecta a otras redes.

![](imagenes_1/isp1.png)
![](imagenes_1/isp2.png)

## DNS
![](imagenes_1/dns1.png)
````
# lunix
ifconfig | grep mask

# Windows y MacOs
ipconfig

# Saber la IP de google
nslookup google.com

# ping a google
ping www.google.com
````
![](imagenes_1/dns2.png)
![](imagenes_1/dns3.png)
![](imagenes_1/dns4.png)


## Primer desarrollo Web
http://info.cern.ch/hypertext/WWW/TheProject.html
Hubo un primer desarrollador Web, su nombre es Tim Berners-Lee.
- 🔹 Hizo la propuesta de W3, la cual es una forma de globalizar la información y poderla linkear.
- 🔹 Todo lo generó a través de una computadora NEXT.
- 🔹 Escribió las 3 tecnologías fundamentales para el desarrollo Web:
    - 🔹 HTML: Lenguaje de marcado para la Web.
    - 🔹 URL: Dirección a la que nos conectamos.
    - 🔹 HTTP: Forma para comunicarnos a través de peticiones
- 🔹 Construyó el primer servidor Web.
- 🔹 Construyó el primer navegador.

![](imagenes_1/web1.png)

## W3C
https://www.w3.org/Consortium/Member/List
![](./imagenes_1/w3c.png)

## Web Browser
Un navegador web es software que nos permite ver y acceder a las paginas web que solicitamos utilizando el **protocolo HTTP** (que basicamente dicta como esa información viajará por Internet). El navegador recibe un documento HTML y muestra la información tal y como se especifica en el html utilizando algo llamado **rendering engine**.

![](imagenes_1/navegador.png)
1[](imagenes_1/navegador2.png)

## HTTP y HTTPs
HTTP son reglas de comunicación.
Para este protocolo existen HTTP Request y HTTP Response, los cuales se encarga del procesamiento de las solicitudes.
⠀
Existen métodos dentro de HTTP:

- **GET**: Solicita datos
- **POST**: Envía datos.
- **PUT**: Crea o reemplaza datos.
- **DELETE**: Borra datos específicos.

![](imagenes_1/http1.png)
![](imagenes_1/http2.png)
![](imagenes_1/http3.png)
![](imagenes_1/http4.png)
![](imagenes_1/http5.png)

## Estandares Web
![](imagenes_1/ew1.png)

## DOM
![](imagenes_1/dom1.png)
![](imagenes_1/dom2.png)

## CSSOM
![](imagenes_1/cssom.png)

## Render Tree
Los árboles CSSOM y DOM se combinan en un árbol de representación. A continuación, este árbol se utiliza para computarizar el diseño de cada elemento visible y sirve como entrada del proceso de pintura que permite representar los píxeles en la pantalla. Para lograr un óptimo rendimiento de representación, es imprescindible optimizar cada uno de estos pasos.

### ¿Qué es el Render Tree?
Es un árbol que une el DOM y CSSOM para renderizarlos, creando un código que pueda interpretar el navegador. De esta manera se generan todas las páginas web que vamos cargando mientras navegamos.
![](imagenes_1/rendertree.png)
![](imagenes_1/rendertree2.png)

### Proceso de renderizado
- **Bytes**: El navegador coge todo el código y lo transforma en bytes.
- **Characters**: El navegador transforma estos bytes en caracteres dependiendo de la codificación que le hemos pasado. Por ejemplo UTF-8.
- **Tokens**: Ahora transforma dichos caracteres en tokens, identificando el significado de los caracteres relacionándolo a etiquetas que generan cierto tipo de contenido. W3C documenta todas la etiquetas.
- **Nodos**: Después de saber el dicho orden de los tokens hará una transformación a los nodos, estos nodos son objetos. Dichos objetos son lo que el navegador sabe interpretar (Los elementos).
- **DOM**: Ya cuando el navegador tiene todos los nodos los ordena en un árbol jerárquico donde cada objeto tendrá una posición dependiendo su etiqueta.
- **CSSROM**: Transforma el CSS y une con el DOM. Asignando los estilos a cada elemento dentro del DOM.

![](imagenes_1/layout.png)
![](imagenes_1/layout2.png)
![](imagenes_1/layout4.png)

## paint
Cuando ya tenemos el **Render Tree** y el **layout** cargados, el proyecto empieza a tomar forma. Mediante el layout se forman las cajas, se llenan con la información y por último se pinta, es decir, se le dan los colores, acabaos, sombras y estilos pertinentes de todos y cada uno de los elementos.

**Paint** o **pintado** es poner los detalles finales para que el proyecto se pueda ver como queríamos al principio. Su velocidad es gran responsable de la velocidad final que se tenga al momento de cargar con el sitio.

![](imagenes_1/paint.png)

## JavaScript Engine
![](imagenes_1/jsengine.png)
- Recibir el código como un flujo de bytes UTF-16 y pasarlo a un decodificador de flujo de bytes (el cual hace parte del motor).
- El parser toma el código y lo descompone en tokens (los tokens son elementos de js como: let, new, símbolos de operaciones, functions, promises).
- Gracias al anterior parseo se genera una estructura de datos en forma de árbol, o Abstract Syntax Tree (AST).
- El intérprete recorre el AST y va generando el bytecode.
- El optimizing compiler optimiza el código bytecode a machine code y se reemplaza el código base.

## Critical rendering path
![](imagenes_1/criticalrenderpath.png)
Todas páginas web están formadas por html, css y Javascript e independienemente de la cantidad de cada uno de ellos, los navegadores siempre siguen el mismo proceso para conseguir tanto el contenido como la manera en que éste se ha de mostrar al usuario:

- Generar el árbol DOM a partir del html.
- Generar el CSSOM Tree a partir del css.
- Generar el Render Tree con la combinación del DOM y - CSSOM
- Calcular la disposición o layout de todos los nodos.
- Pintar los nodos del Render Tree.

![](imagenes_1/critialpath.png)

**El DOM**
Es el árbol de nodos que representa los contenidos de la página o aplicación web. Estos contenidos están determinados por el HTML y, aunque se parezca bastante al DOM, no són lo mismo.

¿Cómo se genera el árbol DOM?
El DOM se genera a partir del fichero con extensión .html y sigue distintos pasos para generarse:

- Convertir los bytes a carácteres.
- Pasar de carácteres a tokens.
- Generar los nodos.
- Construir el árbol DOM.


La construcción del DOM y del CSSOM se hacen de manera asíncrona/paralela. Eso significa que el proceso de generar el CSSOM no es bloqueante para poder generar el DOM, pero, sí que lo es para renderizarlo.

En caso de que el navegador detecte un ````<script>```` no declarado como asíncrono en el ````<head>```` de la página, este será descargado, pero no ejecutado hasta que el árbol CSSOM termine de ser construido y, por tanto, si el **JavaScript** no es ejecutado, la construcción del DOM queda bloqueada.