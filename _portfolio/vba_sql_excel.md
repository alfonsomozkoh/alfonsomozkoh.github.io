---
title: Visual Basic for Applications y SQL server
date: 2014-04-08 00:00:00 Z
tags:
- Godin
- Programación orientada a objetos
- Excel
- VBA
- Visual Basic
- SQL server
layout: post
img: assets/img/portfolio/visual_basic_for_aplications.png
---

![image]({{ site.baseurl }}/{{ page.img }})
Empecemos con algo de contexto

*Advertencia: El siguiente articulo tendrá un corte más ligero y no académico como es común en mis aticulos ya que no me he preocupado por la manera en que redacto, solo soy yo siendo yo, así como escribo este articulo es como me expreso en la vida real.*

### Casi en el final del camino
No hace mucho tiempo que concluyo el semestre, así que tome la decisión de buscar un empleo de medio tiempo para pasar las vacaciones activo además de ahorrar algo de dinero para el siguiente semestre no andar sufriendo las indulgencias del proceso de ser un “ *estudihambre* ”.

Si bien es cierto que desde hace poco más de dos años he sobrevivido desarrollando proyectos independientes como *freelance*, entre más se acerca el momento que concluya mis estudios universitarios me es imperativo conseguir experiencia en el mercado laboral. Ya saben, empezar a hacer carrera de verdad para alcanzar experiencia, una posición buena y en general una mejor calidad de vida lo más pronto posible.

### Mi relación de amor-odio con Microsoft
Durante mi estancia en la universidad la mayoría de las asignaturas enfocadas a la programación o bases de datos eran enseñadas con la ayuda de las tecnologías de  Microsoft Windows, como C++ y C# para la enseñanza de programación orientada a objetos, obviamente el uso de Visual Studio como herramienta principal de desarrollo y SQL server como sistema manejador de base de datos. Claro también se imparte Java para la programación de dispositivos móviles y a veces POO, todo depende de los gustos del profesor.  

Sin embargo son muy pocos los profesores que impulsan el uso de los sistemas GNU/Linux por desconocimiento o simplemente argumentando que en México y Latinoamérica las empresas que basan sus arquitecturas en sistemas de Microsoft Windows  son muy comunes. Por eso  decidí aprender todo lo que se acerca de GNU/Linux  por mi parte con libros y cursos en línea.

Como ya les he podido contado en otros artículos, cuento con una pequeña colección de ordenadores del año del caldo en su hogar, a los cuales tengo divididos en los que funcionan con distros de Linux como [Zorin OS]( https://zorinos.com/), [Xubuntu]( https://xubuntu.org/) y [Deepin OS]( https://www.deepin.org/es/) <3, los que funcionan con Windows 7 Ultimate y Windows 8.1.

Y si te preguntas ¿Por qué no he migrado completamente a Linux? La respuesta es simple; no puedo. No puedo porque mi familia no se acostumbraría al uso de WPS en lugar de Microsoft Office, porque yo mismo no me acostumbro a este cambio, porque más allá de lo divertido que resulta usar sistemas GNU/Linux ser usuario de Windows es sumamente cómodo, así que no odio a Windows, solo no lo amo tanto como antes de ser un amante de GNU/Linux.

<script type="text/javascript">
var bannersnack_embed = {"hash":"bc8eoaljv","width":728,"height":90,"t":1514526375,"userId":33369601,"responsive":true,"type":"html5"};
</script>
<script type="text/javascript" src="//cdn.bannersnack.com/iframe/embed.js"></script>

### El proyecto: Solución para eficientar el proceso de captura de datos para calcular el presupuesto anual. 

Hace dos semanas tuve la oportunidad de entrar a trabajar a una empresa muy *fi fi* diría nuestro futuro presidente como becario en el área de Negocios de TI. ¡Lo cual me tiene muy feliz! Se trata de una empresa química, como *Umbrella* bueno quizá no, pero eso me gusta imaginar. 

Esta empresa química en la que estoy trabajando como becario cuenta con una arquitectura totalmente basada en tecnologías de Microsoft Windows, Microsoft Windows Server 2016, Microsoft Visual Studio 2010, 2012 y 2017, SQL server 2008 R2 y 2013 Microsoft Office 2016, Microsoft OneDrive Enterprise, Skype Enterprise etc. 

El primer reto como *becario fifi* ha sido que me han asignado un proyecto que va de lo siguiente. Se trata de automatizar un proceso de la empresa donde ciertos departamentos  llenan un Excel con la finalidad de calcular sus gastos anuales, para con esos datos proyectar un presupuesto para el siguiente año y presentarlo a los directivos.

Como ya se estarán imaginando, va a optimizar este proceso dentro de la empresa, (*porque se supone que eso hacemos los informáticos, encontramos soluciones a los problemas de las empresas*) en este caso el problema es, el tiempo que tardan en capturar, la poca seguridad que se tiene al manejar un vago archivo de Excel que por su puesto puede ser modificado en cualquier momento y por cualquier persona.

Apuesto que a estas alturas muchos de ustedes ya hasta están visualizando como se vería este proyecto en web con php, o con .Net, sin embargo, cuando me explico mi jefe la situación también me dio los requisitos:

+ El proyecto debe estar listo en un mes o quizá menos.
+ El proyecto debe hacer uso de los recursos de la empresa sin posibilidades de inversiones a corto plazo. ( Es decir que no contamos con capital para la compra de tecnologías extra).
+ El proyecto aún no ha sido presentado por lo que solo existe la idea de la solución.


Obviamente yo me quede con cara de *Watofok!* o sea, no sabía ni que me estaban pidiendo, ni cómo iba a resolverlo, a lo que mi jefe de área respondió con seguridad. - No te apures, sé que estás pensando como un estudiante, yéndote a lo grande, imaginando una solución enorme y super organizada, quizá pensaste en C# o Visual Basic (algunos sistemas de la empresa están fabricados con estas tecnologías) pero no, tienes que pensar en resolver primero el problema, y es por eso que te digo que este proyecto va a ser desarrollado con [Visual Basic for Applications]( https://msdn.microsoft.com/en-us/vba/office-shared-vba/articles/getting-started-with-vba-in-office), si el proyecto es aceptado y tiene una buena recepción, los directivos nos pedirán que lo escalemos y nos darán el presupuesto, no somos una fábrica de software recuerda, eres becario del área de *Negocios de TI*- ¡Boom! ¡Estoy super verde colegas!, tenia razón yo ya estaba super preocupado. 

### La solución 
Para ya no hacer más largo este relato, la solución será construida con las siguientes tecnologías:

+ Visual Basic for Applications
+ Excel
+ SQL server (si en realidad Excel no será donde se almacenen los datos, en realidad solo será el front end, todos los Stored Procedures estarán en la base de datos (DUH! No note lo recursivo que sonó esto hasta que lo edite)) 
+ Autenticación de usuarios por medio del dominio de Windows dentro de la empresa para identificar jerarquías y permisos.

#### Tu opinión es muy importante
Hasta aquí mi avance, cuando hayamos iniciado el desarrollo les iré subiendo más información, de momento, cuéntame; ¿Qué tipo de tecnologías prefieres las de código abierto o propietario?, ¿Crees que en la diversidad esta la riqueza?
Gracias por leerme.