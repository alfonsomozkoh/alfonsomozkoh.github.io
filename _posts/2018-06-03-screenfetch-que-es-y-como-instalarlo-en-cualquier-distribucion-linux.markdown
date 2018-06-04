---
layout: post
title: "ScreenFetch, ¿Qué es y cómo instalarlo en tu distribución GNU/Linux?"
feature-img: "assets/img/pexels/caracteristicas.png"
tags: ["Recomendaciones, Linux, Bash, Terminal"]
author: "Alfonso Mozko H."
---
## ¿Qué es screenfetch?
Screenfetch según Bohnenkamper [1] se trata de:
>  Una "herramienta de información Bash Screenshot". Un práctico script de Bash que se puede utilizar para generar una ingeniosa ficha de que provee información sobre la distribución que se está usando, el tema del terminal, el kernel, el entorno de escritorio, CPU, RAM, y logotipos según la distribución en ASCII que se ven en las capturas de pantalla de todos los días.

En pocas palabras, screenfetch se trata de una aplicación que se ejecuta desde el terminal y muestra una ficha con información relevante de nuestra distribución GNU/Linux ademas de un logotipo de la misma en formato [ASCII](https://es.wikipedia.org/wiki/ASCII) que queda genial y sobre todo muy *informático* al momento de hacer viernes de escrito *guiño guiño*.

## ¿Cómo instalar screenfetch en cualquier distribución Linux?

* Si somos usuarios de **Debian** o sus derivados tendremos que usar:

`sudo apt-get install screenfetch`

* Para los usuarios de **Archlinux** o sus derivados podemos descargarlo directamente de los repositorios oficiales, desde el [AUR](https://aur.archlinux.org/packages/screenfetch-git) o ejecutando el siguiente comando:

`sudo pacman -S screenfetch`

* Para los usuarios de **Fedora** o sus distribuciones derivadas:

`sudo dnf install screenfetch`

* Usuarios de **OpenSUSE**:

`sudo zypper install screenfetch`

* Si utilizas **Solus**:

`sudo eopkg install screenfetch`

* Si eres usuario de **Mac** primero debes instalar [Homebrew](https://brew.sh/) y después ejecutar desde la terminal:

`brew install screenfetch`


Ya que lo hemos instalado podremos ejecutar en la terminal el comando:

`screenfetch`

## Otros usos de Screenfetch

### Realizar una captura de pantalla de los datos mostrados con screenfetch
Si lo que quieres es realizar una captura de pantalla para compartirla en tus redes sociales entonces una vez que hayas instalado screenfetch solo tienes que abrir la terminal y ejecutar el siguiente comando:

`screenfetch -s`


### Que screenfetch se ejecute cada vez que se abre la terminal
Aun que no veo ningún uso práctico,pero pues ¿Quién soy yo para detenerte? asi que YOLO, el comando que estas buscando y debes ejecutar en la terminal es el siguiente:

`sudo nano /etc/bash.bashrc`

Una vez que se abra el editor de textos nano, tenemos que ir a la ultima linea del fichero **bash.bash.rc** y añadir lo siguiente:

`screenfetch`

Después de eso solo guarda el archivo y cierra el editor de texto, a partir de ahora cada vez que abras la terminal aparecerá el logo de tu distro y su respectiva información al lado.

**Para más información acerca del uso de screenfetch** solo hay que consultar en manual ejecutando el siguiente comando:

`man screenfetch`

Espero que esta información haya sido de gran ayuda.
Si conoces como instalar screenfetch en otra distro que no haya mencionado por favor no dudes en compartirla en los comentarios.

## Referencias 
[1] Bohnenkamper, B. (2018). KittyKatt/screenFetch. [online] GitHub. Available at: https://github.com/KittyKatt/screenFetch [Accessed 3 Jun. 2018].


