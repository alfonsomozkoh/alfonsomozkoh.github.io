---
layout: post
title: "Directorios interesantes en Linux  "
feature-img: "assets/img/pexels/directorios-linux.png"
tags: [Informática, Linux, Sistema de Archivos, Terminal]
author: [Alfonso Mozko H.]
---
Linux a diferencia de otros sistemas operativos, tienen una estructura de directorios estándar semejante a la [estructura de árbol invertido]( https://alfonsomozkoh.github.io/2018/06/07/archivos-y-el-sistema-de-archivos-linux.html) que por cierto explico más a fondo en mi [artículo previo]( https://alfonsomozkoh.github.io/2018/06/07/archivos-y-el-sistema-de-archivos-linux.html) . A continuación les presento algunos directorios que merecen mención especial.

## El directorio Raíz  /
En los sistemas Linux hay una y solo una raíz y se denota por el carácter **“/”**. La raíz es el único directorio que no tiene un directorio padre. En este directorio las entradas **“.”** Y **”..”** coinciden.

## /boot
Es en este directorio que se almacena la imagen binaria de arranque del núcleo de Linux; es decir, un archivo que contiene el código del propio sistema operativo Linux. Esta imagen se carga en la memoria nada más iniciar el ordenador y se mantiene ahí hasta que se apaga. El nombre de este archivo depende de la distribución, algunos nombres muy extendidos son: **vmunix, Image, zImage, o vmlinuz.** Es muy importante no borrar nunca este archivo, puesto que si lo hacemos, el sistema no podrá iniciarse más. De hecho, solo el administrador tiene derecho para eliminar este archivo.

## /bin
Llamado así **/bin** por binario, contiene muchas de las órdenes ejecutables utilizadas en Linux. Normalmente aquí se encuentran los programas de uso más común para los usuarios, como la orden **/bin/cp** para copiar los archivos, la orden **/bin/cat** para visualizar archivos de texto  o la orden **/bin/ls** para visualizar los archivos de un determinado escritorio.

## /home
Del directorio **/home** cuelgan los diferentes directorios de trabajo de cada uno de los usuarios. Cada usuario puede hacer lo que guste con su directorio de trabajo, sin embargo, va a tener acceso restringido al resto de directorios. Un usuario normal no va a poder borrar un archivo del directorio raíz o copiar un programa en el directorio **/bin**.

## /usr 
De este directorio colgaban en las primeras versiones de UNIX los subdirectorios de trabajo de los usuarios. En la actualidad el directorio **/usr** contiene también archivos que posteriormente utilizan otras órdenes de Linux. De **/usr** cuelgan también algunos subdirectorios importantes como pueden ser:

+ ### /usr/bin
Contiene programas ejecutables que de alguna forma son mayores en tamaño y se utilizan con menos frecuencia que las órdenes del directorio **/bin**.

+ ### /usr/lib
Contiene archivos de bibliotecas utilizados por los compiladores de lenguajes como FORTRAN, Pascal, C, etc. 

+ ### /usr/man
Contiene las páginas del manual en el disco del ordenador. La orden **man**, de la cual hablaré a fondo en otro artículo, lo único que hace es buscar en este directorio la información solicitada por el usuario y formatearla para que aparezca adecuadamente en la terminal.

+ ### /usr/local/bin  y /usr/contrib/bin
Directorios generalmente creados por los administradores del sistema para contener archivos ejecutables que forman parte de Linux. Cualquier usuario (osado) que desarrolle una nueva utilidad, puede dejarla en uno de los dos directorios anteriores de modo que sea accesible al resto de los usuarios.

## /etc
Directorio que contiene órdenes y archivos de configuración empleados en la administración del sistema. Están guardadas en un directorio aparte debido a que la mayoría de ellas solo pueden ser ejecutadas por usuarios privilegiados. Normalmente, todos los archivos de configuración presentes en Linux son archivos de texto. La razón es que de este modo son fáciles de interpretar y de modificar, para lo cual utilizaremos sólo un editor de texto.

## /dev
Directorio que contiene los archivos de dispositivos empleados para la comunicación con dispositivos periféricos, tales como impresoras, discos, terminales, etc. Un **archivo de dispositivo** es un archivo especial, reconocido por el núcleo, que representa a un elemento de entrada – salida (E/S). La idea es tratar los dispositivos de E/S como si se tratará de archivos, es algo que se conoce con el nombre de [independencia de dispositivo](https://es.wikipedia.org/wiki/Independencia_de_dispositivos).  La independencia de archivos es algo muy interesante y muy utilizado, porque de este modo emplearemos las mismas funciones tanto para trabajar con archivos ordinarios como para trabajar con elementos de E/S.
 
