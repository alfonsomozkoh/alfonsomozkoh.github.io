---
layout: post
title: "Una breve introducción SOA, ROA y REST"
tags: ["Programación, SOA, ROA"]
authors: ["Yazmin Pedraza O.","Luis G. López R.","Rogelio Ramírez R.","Alfonso Mozko H." ]
---
## Service Oriented Architecture
Arquitectura orientada a servicios en español, fue descrita por primera vez por Gartner en 1996. SOA fue evolucionando desde que fueron Web Services con estándares de transferencia XML a SOA que incorpora XML, SOAP, WSDL, UDDI, Bus. Morales [1] comenta,
>“SOA es un modelo arquitectónico de software creado y usado para diseñar modelos de negocio empaquetados como servicios”.

SOA proporciona una metodología y un marco de trabajo basado en servicios, el objetivo es proveer la reutilización de un determinado servicio evitando el desarrollo de  interfaces, lo cual permite proveer ventaja en la construcción de sistemas distribuidos. Salvador [2] afirma,
>“Una Arquitectura Orientada a Servicio está compuesta por elementos
funcionales y elementos relacionados con la calidad de servicio”.

ROA Arquitectura Orientada a Recursos es un estilo arquitectónico basado en REST, su principal función es exponer recursos. Según Guevara [3]
>“Toda implementación  de ROA es a su vez una implementación de SOA pero lo opuesto no es cierto”.

Esta arquitectura pretende ser un método sistemático para desarrollar servicios en la Web que se adhieran a los principios de REST, la identificación de recursos aparece como un elemento esencial, un recurso consiste en una entidad que será lo suficientemente importante para ser referenciada, cada recurso debe tener al menos un único punto de acceso que lo distinga de otros, esta referencia única se llama URIs( Uniform Resource Identifier), las URIs de los recursos permiten que éstos se interrelacionen, formando una red interconectada navegable por agentes electrónicos, tal como funciona la web.

REST (Representational State Transfer) es un estilo arquitectónico para sistemas hipermedia distribuidos tales como la web.

### Referencias

[1] Carlos Andrés Morales Machuca. (2014, Febrero) http://studylib.es. [Online].
http://studylib.es/doc/8717090/estado-del-arte--servicios-web
 
[2] Salvador Otón Tortosa, Antonio Ortiz Baillo, and José Ramón Hilera González. (2006,
Mayo) Universidade Federal do Rio Grande do Sul. [Online].
http://www.ufrgs.br/niee/eventos/RIBIE/2006/ponencias/art044.pdf

[3] Angel Guevara. (2017, Marzo) Speaker Deck. [Online].
https://speakerdeck.com/faryshta/terminologia-roa