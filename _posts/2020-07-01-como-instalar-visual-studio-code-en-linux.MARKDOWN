---
title: "¿Cómo instalar Visual Studio Code en Linux?"
date: 2020-07-01 00:00:00 Z
tags:
- visual studio code
- visual studio ide
- visual studio professional 
- visual studio community 
- visual studio linux
- visual studio on linux
- linux c#
- visual studio 2019
- visual studio community
layout: post
feature-img: assets/img/pexels/VSCvsVS.gif
author:
- Alfonso Mozko H.
---

## ¿Son lo mismo Visual Studio Code que Visual Studio?
Desarrollado por Microsoft en 1997, Visual Studio es un IDE para Windows y Mac que permite a los desarrolladores desarrollar aplicaciones y escribir código utilizando una miríada de lenguajes de programación como C, C++, Python, Go y Java, por mencionar algunos.

Por otro lado, Visual Studio Code fuel lanzado en 2015, es un editor de código libre y de código abierto, multiplataforma, que está disponible en Linux.

Si deseas conocer todas las diferencias entre Visual Studio (Community, Professional y Enterprise) te recomiendo este articulo que escribí hace algún tiempo: [¿Cuál es la diferencia ente Visual Studio y Visual Studio Code?](https://alfonsomozkoh.github.io/2018/08/31/cual-es-la-diferencia-entre-visual-studio-y-visual-studio-code.html).

## ¿Cómo instalar Visual Studio Code en Linux?
En este artículo, te guiare a través de la instalación de código de Visual Studio en Linux con los comandos y el paso a paso que deberás seguir. Para ser más específico, aprenderás cómo instalar el código de Visual Studio tanto en distribuciones de Linux basadas en Debian como en RedHat.

## ¿Cuáles son los comandos para instalar Visual Studio en Debian, Ubuntu y Linux Mint?
El método preferido para instalar Visual Code Studio en sistemas basados en Debian es habilitar el repositorio de código VS Code e instalar el paquete de código de Visual Studio Code usando el administrador de paquetes apt.

	$ sudo apt update

Una vez actualizado, podemos proceder e instalar las dependencias necesarias para la ejecución.
	
	$ sudo apt install software-properties-common apt-transport-https

A continuación, usando el comando wget, importa la llave GPG de Microsoft como se muestra:
	
	$ sudo wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -

Con la adición de la llave GPG de Microsoft, habilita el repositorio de código de Visual Studio ejecutando el comando:

	$ sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"

Una vez que hayas habilitado el repositorio, actualiza el sistema e instala el código de Visual Studio Code ejecutando el siguiente 
comando:

	$ sudo apt update
	$ sudo apt install code

Debido a su tamaño, y a que no son enchiladas, la instalación tarda aproximadamente 5 minutos. Una vez instalado, puedes utilizar el administrador de aplicaciones para buscar Visual Studio Code y lanzarlo.


![visual-studio-code-en-linux]({{ site.baseurl }}/assets/img/pexels/instalar-visual-studio-en-ubuntu.png)


[![Gana-Bitcoins-Con-Anuncios-En-Tu-Web][1]][2]
[1]: {{ site.baseurl }}/assets/img/pexels/a-ads-referido.gif
[2]: https://a-ads.com?partner=1416871 




