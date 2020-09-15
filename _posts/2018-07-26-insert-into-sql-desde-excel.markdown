---
title: "¿Cómo crear una sentencia INSERT INTO en Excel para SQL?"
date: 2018-07-26 00:00:00 Z
tags:
- SQL
- Excel
- SQL Server Management Studio
- phpMyAdmin
- Concatenar
layout: post
feature-img: assets/img/pexels/insertinto_con_ayuda_de_excel.png
thumbnail: assets/img/pexels/insertinto_con_ayuda_de_excel.png
author:
- Alfonso Mozko H.
---

Imagina esta situación: Tienes la necesidad de insertar una cantidad muy grande de datos; Estos datos pueden ser precios, direcciones, usuarios, etc. Y los quieres insertar en una base de datos (MySQL, MSSQL, POSTGRESQL,o cualquier otra con soporte estándar.


Hace poco me encontré en una situación que me obligo a pensar en la siguiente solución, hoy la quiero compartir contigo y saber tu opinión. Espero que te sea de mucha ayuda.


### Algo de contexto
Ahí me encontraba yo, llenando una base de datos con registros de prueba para dar inicio a las pruebas de un proyecto que estoy realizando para VBA. Todo iba muy bien hasta que llegó el momento de llenar una tabla que constaba un total de 32,349 filas en total.  Nunca me había encontrado en una situación así, pensé en la manera más sencilla de hacer ese tremendo INSERT INTO mi tabla, al final decidí apoyarme con Excel.

### La solución: Crear una tabla en Excel con la misma estructura que la tabla de tu base de datos y hacer uso de la función CONCATENAR
Imagina que tienes una tabla en base de datos llamada *Tbl007_GastoBase_Viaje* que contiene los gastos en viáticos de una "X" compañía. Esta tabla tiene las siguientes columnas.

![insertinto_excel_sql]({{ site.baseurl }}/assets/img/pexels/tabla-sql.png)

Lo primero que debes hacer es crearte una tabla en Excel con la misma estructura, y me refiero a que los nombres de las columnas deben ser exactamente iguales.

![insertinto_excel]({{ site.baseurl }}/assets/img/pexels/insert-into-excel.png)

En mi caso, el contenido de la tabla creada en la hoja de Excel con las mismas columnas que la tabla en mi base de datos, abarca desde la celda **A2** hasta la celda **K2** de ancho y de ahí hacia abajo. Ahora nos posicionamos en la celda **L2** e introducimos lo siguiente:

``=+CONCATENAR("INSERT INTO Tbl007_GastoBase_Viaje VALUES(ID,Ruta,Tipo,Repro,Ppto,Ciudad_Destino,Hospedaje_Repro,Hospedaje_Ppto,Comida_Repro,Comida_PPTO,Moneda)('",B2,"','",C2,"',",D2,",",E2,",'",F2,"',",G2,",",H2,",",I2,",",J2,",'",K2,"')")``

Nota que la función que indicamos ``=+CONCATENAR(INSERT INTO(Campos_de_tu_tabla) VALUES (Coordenadas_de_excel)`` nos permite crear una sentencia **INSERT INTO** de **SQL** y el resultado es el siguiente:

``INSERT INTO Tbl007_GastoBase_Viaje(ID,Ruta,Tipo,Repro,Ppto,Ciudad_Destino,Hospedaje_Repro,Hospedaje_Ppto,Comida_Repro,Comida_PPTO,Moneda) VALUES ('GDL-MEX-CME-MEX-GDL','Nacional',4489,4646,'CIUDAD DEL CARMEN',0,0,750,750,'MXN')``

Ya con los datos que deseamos INSERT INTO nuestra base de datos, lo que debes hacer ahora es copiar y pegar esta función hacia abajo, de manera que se vayan creando tantos INSERT INTO como filas tengas en tu tabla de Excel. El resultado será algo así más o menos:

``=+CONCATENAR("INSERT INTO Tbl007_GastoBase_Viaje(ID,Ruta,Tipo,Repro,Ppto,Ciudad_Destino,Hospedaje_Repro,Hospedaje_Ppto,Comida_Repro,Comida_PPTO,Moneda) VALUES ('",B2,"','",C2,"',",D2,",",E2,",'",F2,"',",G2,",",H2,",",I2,",",J2,",'",K2,"')")``

``=+CONCATENAR("INSERT INTO Tbl007_GastoBase_Viaje(ID,Ruta,Tipo,Repro,Ppto,Ciudad_Destino,Hospedaje_Repro,Hospedaje_Ppto,Comida_Repro,Comida_PPTO,Moneda) VALUES ('",B3,"','",C3,"',",D3,",",E3,",'",F3,"',",G3,",",H3,",",I3,",",J3,",'",K3,"')")``

``=+CONCATENAR("INSERT INTO Tbl007_GastoBase_Viaje(ID,Ruta,Tipo,Repro,Ppto,Ciudad_Destino,Hospedaje_Repro,Hospedaje_Ppto,Comida_Repro,Comida_PPTO,Moneda) VALUES ('",B4,"','",C4,"',",D4,",",E4,",'",F4,"',",G4,",",H4,",",I4,",",J4,",'",K4,"')")``

Si seleccionas y copias todas esas celdas que contienen esta estructura el resultado será el siguiente:

``INSERT INTO Tbl007_GastoBase_Viaje(ID,Ruta,Tipo,Repro,Ppto,Ciudad_Destino,Hospedaje_Repro,Hospedaje_Ppto,Comida_Repro,Comida_PPTO,Moneda VALUES ('GDL-MEX-CME-MEX-GDL','Nacional',4489,4646,'CIUDAD DEL CARMEN',0,0,750,750,'MXN')``

``INSERT INTO Tbl007_GastoBase_Viaje(ID,Ruta,Tipo,Repro,Ppto,Ciudad_Destino,Hospedaje_Repro,Hospedaje_Ppto,Comida_Repro,Comida_PPTO,Moneda VALUES ('GDL-MEX-GDL','Nacional',3816,3949,'MEXICO',1750,1811,750,750,'MXN')``

``INSERT INTO Tbl007_GastoBase_Viaje(ID,Ruta,Tipo,Repro,Ppto,Ciudad_Destino,Hospedaje_Repro,Hospedaje_Ppto,Comida_Repro,Comida_PPTO,Moneda VALUES ('GDL-MEX-GRU-MEX-GDL','Internacional',29578,30613,'SAO PAOLO ',0,352,1500,1500,'MXN')``

Ahora ya tienes todo listo para hacer tu mega INSERT INTO dentro de tu tabla, lo puedes hacer con SQL Server Management Studio, phpMyAdmin, o con cualquier manejador de bases de datos.

También puedes crear un Script más avanzado donde establezcas el uso de la Base de Datos y ejecutarlo como tal. Sin embargo considero que esta es una solución rápida y más accesible para todos aquellos que no sean expertos en las artes oscuras de SQL. Lo importante aquí es que puede INSERT INTO mi tabla de mi base de datos 32,349 filas sin morir en el intento.

Espero que esta información haya sido de ayuda para ti. Si tienes una mejor idea para hacer INSERT INTO masivos en una tabla de tu base de datos con el uso de Excel compártela en los comentarios por favor :D
