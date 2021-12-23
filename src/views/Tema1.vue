<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5
    .titulo-principal
      .titulo-principal__numero
        span 1
      h1 Introducción a NoSQL
    
    figure
      img(src="@/assets/template/tema-1-1.png", alt="Texto que describa la imagen")
    p.mt-4 NoSQL (“no SQL”) comprende una amplia clase de sistemas de gestión de bases de datos que difieren del modelo clásico de SGBDR (Sistema de Gestión de Bases de Datos Relacionales) en aspectos importantes, siendo el más destacado que no usan SQL como lenguaje principal de consultas. #[strong (Wikipedia, 2021a).]
    .bloque-texto-a.color-acento-botones.p-4.p-md-5.mb-5 
      .row.m-0.align-items-center.justify-content-between
        .col-lg-8
          .bloque-texto-a__texto.p-4
            p Los datos almacenados no requieren estructuras fijas, como tablas; normalmente, no soportan operaciones JOIN ni garantizan completamente ACID (atomicidad, consistencia, aislamiento y durabilidad), y, habitualmente, escalan bien horizontalmente, es decir, pueden ir aumentado la estructura de manera sencilla. Los sistemas NoSQL se denominan, a veces, “no solo SQL” para subrayar el hecho de que también pueden soportar lenguajes de consulta de tipo SQL. #[strong (Wikipedia, 2021a).]
        .col-lg-4.mb-4.mb-lg-0
          figure
            img(src="@/assets/template/tema1-2.svg", alt="Texto que describa la imagen") 
    
    .titulo-segundo.mt-5
      #t_1_1.h4 1.1  Definición de NoSQL
    .row.mt-4
      .col-12.col-lg-8
        p La web 2.0 (donde quienes suministran el contenido son los usuarios) trajo grandes necesidades de datos e infraestructura tecnológica, principalmente, para empresas como Google, Amazon y Facebook. Ellos tuvieron que buscar soluciones propias a estos problemas, enfocados en la gran cantidad de almacenamiento y el crecimiento de sistemas web con acceso a información en tiempo real, donde surgió la necesidad de proporcionar información gestionada y procesada desde grandes volúmenes de datos. Debido a que las bases de datos relacionales no responden de forma adecuada a esta necesidad, para la exigencia en tiempos de demanda, nacen las bases de datos NoSQL.
      .col-4.offset-4.offset-lg-0.align-self-center
        figure
          img(src="@/assets/template/tema1-3.png", alt="Texto que describa la imagenalt")
    p.mt-5 Se deben definir algunos conceptos técnicos de suma importancia:    
    .row.mt-5
      .col-
        //- LineaTiempoD debe ir acompañado de una de una de estas clases => 
        //- .color-primario, .color-secundario, .color-acento-contenido, .color-acento-botones
        LineaTiempoD.color-primario
          p.text-small(numero="1" titulo="Escalabilidad") Es la capacidad que tiene un sistema de ser configurado en software o hardware, para mejorar la respuesta a las exigencias o nuevas demandas de capacidad de procesamiento o almacenamiento (conservando las mismas funcionalidades). Actualmente, se usa mucho el término ‘escalabilidad vertical’, para referirse a este tipo de escalabilidad. 
          
          p.text-small(numero="2" titulo="Escalabilidad horizontal") Consiste en potenciar el rendimiento del sistema desde un aspecto de mejora global, a diferencia de aumentar la potencia de una única parte del mismo. Este tipo de escalabilidad se basa en la modularidad de su funcionalidad (Junta de Andalucía, s. f.), es decir, que las funcionalidades se puedan extender con la misma facilidad con la que mejoran el rendimiento y capacidad.
          
          p.text-small(numero="3" titulo="Escalabilidad vertical y horizontal") Las bases de datos no relacionales están diseñadas para ofrecer sistemas con altas capacidades de escalabilidad vertical y horizontal.

    .titulo-segundo.mt-5
      #t_1_2.h4 1.2  Cómo diferenciar NoSQL de SQL
    .row.mt-5
      .col-12.col-lg-8.align-self-center
        p Al utilizar el término NoSQL no se hace referencia a una base de datos o a un tipo de base de datos, sino que, más bien, es la definición de un conjunto de tipos de bases de datos que son diferentes a las bases de datos convencionales (relacionales). La principal diferencia entre las bases de datos de NoSQL y las bases de datos relacionales tradicionales es que las NoSQL emplean una forma de almacenamiento no estructurado o de estructuras diferentes a tablas. Simplificando la estructura de almacenamiento, es así como las NoSQL pueden concentrarse en procesar grandes volúmenes de datos.
      .col-4.col-lg-3.offset-4.offset-lg-0.align-self-center
        figure
          img(src="@/assets/template/tema1-4.svg", alt="Texto que describa la imagen")
    p.mt-2 A continuación, se muestra una comparación rápida de las funciones de NoSQL con las bases de datos relacionales.
    .row.mt-5
      .col-8.offset-2
        .h4 Tabla 1
        .tabla-a.color-acento-botones.mt-4.scroll-x-tabla 
          table
            caption Comparación de las funciones de NoSQL
            thead
              tr
                th Característica
                th Base de datos NoSQL
                th Bases de datos relacionales
            tbody.text-center
              tr
                td.py-3 Desempeño
                td Alto
                td Bajo
              tr
                td.py-3 Fiabilidad
                td Pobre
                td Buena
              tr
                td.py-3 Disponibilidad
                td Buena
                td Buena
              tr
                td.py-3 Consistencia 
                td Pobre
                td Buena
              tr
                td.py-3 Almacenamiento de datos
                td Optimizado para muchos datos
                td Mediano o grande
              tr
                td.py-3 Estabilidad
                td Alta
                td Alta (pero más costosa)
    p.mt-5 A continuación, se presentan algunas ventajas y desventajas que tiene cada uno de estos tipos de bases de datos:
    .row.mt-5
      .col-12
        .tabla-a.color-primario.mt-4.scroll-x-tabla  
          table
            
            thead
              tr
                th Ventajas
                th Desventajas
            tbody
              tr
                td.p-0
                  figure
                    img(src="@/assets/template/tema1-5.png", alt="Texto que describa la imagen")
                td.p-0 
                  figure
                    img(src="@/assets/template/tema1-6.png", alt="Texto que describa la imagen")
              tr
                td.py-3 
                  p Contrario a las bases de datos relacionales, las NoSQL están basadas en key-value pairs (clave valor).
                  p.mt-3 Las NoSQL tienen diferentes tipos de almacenamiento, como el almacén de columnas, documentos, claves, valor de gráficos (capas), objetos, en formato XML y otros modos de tipos de datos. Las bases de datos NoSQL de código abierto tienen una implementación rentable económicamente, al no requerir licencias ni hardware de precio alto.
                  p.mt-3 Trabajando con bases de datos NoSQL, la expansión de funcionalidades es más fácil y más económica que usando bases de datos relacionales. 
                td.py-3
                  p Casi todas las bases NoSQL no admiten funciones de fiabilidad o integridad de los datos, mientras que las bases de datos relacionales, sí. Las bases NoSQL no soportan las funcionalidades o restricciones de consistencia en los datos. Para garantizar la integridad, es responsabilidad de los desarrolladores implementar con código propio, lo que agrega más complejidad al sistema.
                  p.mt-3 La falta de integridad referencial en los datos hace que no sean fiables para realizar transacciones seguras, como en los sistemas bancarios, donde la integridad de los datos es primordial. Otras formas de complejidad encontradas en la mayoría de las bases de datos NoSQL incluyen la incompatibilidad con consultas SQL; se necesita un lenguaje de consulta manual, haciendo los procesos mucho más lentos y complejos.
    .titulo-segundo.mt-5
      #t_1_3.h4 1.3  Tipos de bases de datos NoSQL
    p.mt-4 Dentro de las bases de datos no relacionales, se encuentran distintos modelos o tipos de implementaciones. Este grupo de bases de datos no relacionales NoSQL desempeñan funciones para diferentes ambientes, en particular, y con necesidades también diferentes.
    figure
      img(src="@/assets/template/tema1-7.png", alt="Texto que describa la imagen")
    p.mt-4 Existen algunos tipos más comunes que otros, ya que están orientadas a documentos, por permitir mejor escalabilidad horizontal #[strong (Macarrón, 2021).]
    .h4.mt-5 Bases de datos basadas en clave valor.
    p.mt-4 Las bases de datos basadas en clave valor son un tipo de base de datos NoSQL sencillo, que sirve para insertar y consultar datos. El concepto ‘clave valor’ significa que los datos se almacenan como una colección de pares clave-valor; la clave identifica de forma única la colección y el valor contiene los datos, y se ordenan según la clave.
    figure.mt-5
      img(src="@/assets/template/tema1-8.png", alt="Texto que describa la imagen")
    .h4.mt-4 Ejemplo
    p.mt-4 Supóngase que se quieren almacenar datos de una persona, como su cédula, nombres, apellidos, correo y varios números de teléfono, y que, por ejemplo, necesita guardar los datos para las siguientes personas:
    .row.mt-5
      .col-10.offset-1
        .h4 Tabla 2
        .row
          .col-8
            p.mt-4 Ejemplo 1 de base de datos
            .row
              .col-6
                ul.lista-ul--color
                  li 
                    i.fas.fa-database
                    p.mb-0 #[strong Cédula:] 1029283762
                  li
                    i.fas.fa-database
                    p.mb-0 #[strong Nombre:] JUAN CARLOS
                  li  
                    i.fas.fa-database
                    p.mb-0 #[strong Apellidos:] MARTINEZ
                  li  
                    i.fas.fa-database
                    p.mb-0 #[strong Correo:] juancho@nerss.et
                  li  
                    i.fas.fa-database
                    p.mb-0 #[strong Teléfono:] 3150817273
                  li  
                    i.fas.fa-database
                    p.mb-0 #[strong Teléfono:] 3168272372
              .col-auto
                ul.lista-ul--color
                  li 
                    i.fas.fa-database
                    p.mb-0 #[strong Cédula:] 98765322
                  li
                    i.fas.fa-database
                    p.mb-0 #[strong Nombre:] DANIELA
                  li  
                    i.fas.fa-database
                    p.mb-0 #[strong Apellidos:] VELEZ LEMOS
                  li  
                    i.fas.fa-database
                    p.mb-0 #[strong Correo:] dnala@nerss.et             
          .col-4
            figure
              img(src="@/assets/template/tema1-9.svg", alt="Texto que describa la imagen")
    p.mt-4 Se toma la cédula como una especie de llave para identificar a una persona, es decir, la cédula es el identificador único para cada persona y no hay dos personas con la misma cédula.
    .h4.mt-5 Más posibilidades
    p.mt-4 En la misma base de datos, se necesita guardar datos de carros, siendo la placa lo que permite identificar al vehículo; entonces, los datos a guardar serían:
    .row.mt-4
      .col-4.col-lg-2.rounded-10.bg-amarillo.p-4
        p.mb-0 #[strong Placa:] MSR-13
        p.mb-0.mt-1 #[strong Modelo:] 2015 
        p.mb-0.mt-1 #[strong Marca:] MAZDA
        p.mb-0.mt-1 #[strong Tipo:] SEDAN
    .h4.mt-5 La base de datos sería: 
    .row.mt-4
      .col-8.offset-2.offset-lg-3
        .h4 Tabla 3
        p Ejemplo 2 de base de datos
        .tabla-a.color-acento-botones.mt-4.scroll-x-tabla  
          table
            caption 
            thead
              tr
                th Clave
                th Valor
            tbody.text-center
              tr
                td.py-3 persona/cedula
                td 1029283762
              tr
                td.py-3 persona/1029283762/apellidos
                td MARTINEZ
              tr
                td.py-3 persona/1029283762/correo
                td juancho@nerss.et
              tr
                td.py-3 persona/1029283762/telefono
                td 3150817273
              tr
                td.py-3 persona/1029283762/telefono
                td 3150817273
              tr
                td.py-3 carro/placa
                td MSR-13
              tr
                td.py-3 carro/MSR-13/modelo
                td 2015
              tr
                td.py-3  carro/MSR-13/marca
                td MAZDA
              tr
                td.py-3 carro/MSR-13/tipo
                td SEDAN
              tr
                td.py-3 persona/cedula
                td 98765322
              tr
                td.py-3 persona/98765322/nombres
                td DANIELA
              tr
                td.py-3  persona/98765322/apellidos
                td VELEZ LEMOS
              tr
                td.py-3 persona/98765322/correo
                td dnala@nerss.et
    p.mt-4 Estas bases de datos son óptimas para consultas en ambientes de respuesta rápida, para aplicaciones de tiempo real, como sistemas de telefonía IP o sistemas de chats.
    .h4.mt-5 Bases de datos orientadas a documentos.
    .row.mt-5
      .col-10.offset-1
        .bloque-texto-g.color-acento-botones.p-3.p-sm-4.p-md-5.mb-5
          .bloque-texto-g__img(
            :style="{'background-image': `url(${require('@/assets/template/tema1-10.png')})`}")
          .bloque-texto-g__texto.p-4
            p.mb-0 Los SGBD con estas características son denominadas bases de datos documentales, funcionan en el marco de la definición de un “documento”; la mayoría de estos SGBD coinciden en cómo se almacena la información, empleando un formato estándar. Los formatos estándares más comunes o populares son JSON, BSON y XML. Se podría considerar este último tipo de formato como el más utilizado en la actualidad.
    .row.mt-5
      .col-10.offset-1
        .tarjeta-avatar-b.mb-5
          img(src='@/assets/template/tema1-11.svg' alt='AvatarTop' style="position:relative").w-15
          .tarjeta.borde-gris
            .p-4
              h2 Formato XML
              p XML, sigla en inglés de eXtensible Markup Language, traducido como “Lenguaje de Marcado Extensible” o “Lenguaje de Marcas Extensible”, es un metalenguaje que permite definir lenguajes de marcas, desarrollado por el World Wide Web Consortium (W3C), utilizado para almacenar datos en forma legible. Proviene del lenguaje SGML y permite definir la gramática de lenguajes específicos (de la misma manera que HTML es, a su vez, un lenguaje definido por SGML) para estructurar documentos grandes. A diferencia de otros lenguajes, XML da soporte a bases de datos, siendo útil cuando varias aplicaciones deben comunicarse entre sí o integrar información. #[strong (Wikipedia, 2021).]
    .h4.mt-5 Modelar información.
    p.mt-5 Suponga que se desea modelar la información contenida en un mensaje de correo electrónico.
    .row.mt-5 
      .col-12.col-lg-10.col-xl-8.offset-lg-1.offset-xl-2
        .h4 Figura 1
        p.mt-4 Modelación de información
        .row.mt-5.rounded.bg-gris.p-5.font-console
          .col-12
            p.mb-0 &lt;Edit_Mensaje&gt;
          .col-11.offset-1
            p.mb-0 &lt;Mensaje&gt;
          .col-10.offset-2
            p.px-3.mb-0 &lt;Remitente&gt;
          .col-9.offset-3
            p.px-3.mb-0 &lt;Nombre&gt;Nombre del remitente&lt;/Nombre&gt;
            p.px-3.mb-0 &lt;Mail&gt;Correo del remitente&lt;/Mail&gt;
          .col-10.offset-2
            p.px-3.mb-0 &lt;/Remitente&gt;
            p.px-3.mb-0 &lt;Destinatario&gt;
          .col-9.offset-3
            p.px-3.mb-0 &lt;Nombre&gt;Nombre del destinatario&lt;/Nombre&gt;
            p.px-3.mb-0 &lt;Mail&gt;Correo del destinatario&lt;/Mail&gt;
          .col-10.offset-2
            p.px-3.mb-0 &lt;/Destinatario&gt;
            p.px-3.mb-0 &lt;Texto&gt;          
          .col-9.offset-3
            p.px-3.mb-0 &lt;Asunto&gt;
          .col-8.offset-4
            p.px-3.mb-0 Este es mi documento con una estructura muy sencilla no contiene atributos ni entidades…
          .col-9.offset-3
            p.px-3.mb-0 &lt;/Asunto&gt;
            p.px-3.mb-0 &lt;Parrafo&gt;
          .col-8.offset-4
            p.px-3.mb-0 Este es mi documento con una estructura muy sencilla no contiene atributos ni entidades…
          .col-9.offset-3
            p.px-3.mb-0 &lt;/Parrafo&gt;
          .col-10.offset-2
            p.px-3.mb-0 &lt;/Texto&gt;
          .col-11.offset-1
            p.mb-0 &lt;/Mensaje&gt;
          .col-12
            p.mb-0 &lt;/Edit_Mensaje&gt;
        figcaption.mt-3.mx-0 Nota. Tomada de Wikipedia (2021).
    .h4.mt-5 En base de datos relacional
    p.mt-5 Si se quisiera modelar esto en una base de datos relacional, seguramente se definiría una tabla para personas (con atributos nombre y correo) y una tabla para los correos, con dos relaciones a la tabla personal: una para el remitente y otra para el destino.
    .row.mt-4
      .col-5.col-lg-3.rounded-10.bg-azul.p-4
        p.mb-0 #[strong Persona:]  (nombres, correo)
        p.mb-0.mt-1 #[strong Correo:] (asuntos y texto) 
    p.mt-5 Sin embargo, en XML, en lugar de tener filas en las tablas, cada correo es un archivo con la estructura dada en el ejemplo.
    .row.mt-5
      .col-10.offset-1
        .tarjeta-avatar-b.mb-5
          img(src='@/assets/template/tema1-12.svg' alt='AvatarTop' style="position:relative")
          .tarjeta.borde-gris
            .p-4
              h2 Formato JSON
              p JSON (acrónimo de JavaScript <i>Object Notation</i>, «notación de objeto de JavaScript») es un formato de texto sencillo para el intercambio de datos. Se trata de un subconjunto de la notación literal de objetos de JavaScript, aunque, debido a su amplia adopción como alternativa a XML, se considera (año 2019) un formato independiente del lenguaje (Wikipedia, 2021).
    .row.mt-5
      .col-10.offset-1
        //- LineaTiempoD debe ir acompañado de una de una de estas clases => 
        //- .color-primario, .color-secundario, .color-acento-contenido, .color-acento-botones
        LineaTiempoD.color-acento-botones
          p.text-small(numero="1" titulo="Cadenas de texto") Al ser una secuencia de ninguno o más caracteres, se ponen entre doble comilla, cómo en lenguaje JavaScript. Ejemplo: “Hola Mundo” 

          p.text-small(numero="2" titulo="Números") Se permiten números negativos y positivos, que también pueden contener parte no entera separada por puntos. Ejemplo: 654.321

          p.text-small(numero="3" titulo="Arreglos") Representan una lista con ninguno o más valores, los cuales pueden ser todos del mismo o de diferente tipo. Los valores separados por comas y el vector, entre llaves ([]). Ejemplo [“Luis”,”Carlos”,”Julian”,99] 

          p.text-small(numero="4" titulo="Booleanos") Representan valores booleanos y pueden tener dos valores: <i>true y false</i>

          p.text-small(numero="5" titulo="Valores nulos") Representan el valor nulo (<i>null</i>)

          p.text-small(numero="6" titulo="Objetos") Son colecciones no ordenadas de pares de la forma &lt;nombre&gt;:&lt;valor&gt;, donde el nombre debe ser separado por comas y puestos entre corchetes ({})
    .h4.mt-5 Bases de datos no relacionales no documentadas
    p.mt-4 Las bases de datos no relacionales documentales y su concepto de guardar la información con el modelo clave/valor. Es por eso que los documentos más comunes son en formato JSON. La diferencia radica en que un documento se almacena en una clave. Esta definición puede parecer abstracta, se explica mejor con un ejemplo:
    .row.mt-5 
      .col-12.col-lg-10.col-xl-8.offset-lg-1.offset-xl-2
        .h4 Figura 2
        p.mt-4 Representación de los datos de una persona en un documento
        .row.mt-5.rounded.bg-gris.p-5.font-console
          .col-12
            p.mb-0 {
          .col-11.offset-1
            p.mb-0 "nombres" : "JUAN CARLOS",
          .col-11.offset-1
            p.mb-0 "apellidos" : "MARTINEZ",
          .col-11.offset-1
            p.mb-0 "fecha_nacimiento" : "1995-05-15",
          .col-11.offset-1
            p.mb-0 "edad" : 65,
          .col-11.offset-1
            p.mb-0 "saldo" : 9876.134,
          .col-11.offset-1
            p.mb-0 "hobbies" : ["música","futbol","leer"],
          .col-11.offset-1
            p.mb-0 "correo" : "juancho@nerss.et",
          .col-11.offset-1
            p.mb-0 "pedidos" : [],
          .col-11.offset-1
            p.mb-0 "acreedores" : null
          .col-12
            p.mb-0 }
    figcaption.mt-4 Note cómo “nombres” es la clave y “JUAN CARLOS” es el valor. De la misma forma como “edad” es la clave y 65 el valor.
    .h4.mt-5 Ejemplo
    p.mt-4 Suponga que necesita modelar un menú de una aplicación como se muestra a continuación:
    .row.mt-5
      .col-6.col-lg-3.offset-2.offset-1
        .h4 Figura 3
        p.mt-4 Ejemplo
        figure.mt-4
          img(src="@/assets/template/tema1-13.png" alt="Texto que describa la imagen")
    .row.mt-5
      .col-10.offset-1
        .tarjeta-avatar-b.mb-5
          img(src='@/assets/template/tema1-14.svg' alt='AvatarTop' style="position:relative")
          .tarjeta.borde-gris
            .p-4
              h2 Representación en formato BSON
              p La representación de JSON que se muestra en esta tabla es una representación en formato texto, pero también se puede representar en formato binario (unos y ceros); a esta otra representación equivalente en binario se le llama BSON. Es una cadena de unos y ceros sin nada que la caracterice de más, excepto que al convertirla en cadenas de texto se presenta como se observó en el ejemplo
    .h4.mt-4 Tabla 4
    p.mt-4 Ejemplo
    .row.mt-4
      .col-12
        tabla-a.color-primario.mt-4 
          table
            caption 
            thead
              tr
                th Su representación en XML
                th Su equivalente en JSON
            tbody
              tr
                td.p-4 
                  .row
                    .col-12
                      .row
                        .col-12.rounded.bg-gris.py-5.px-3.font-console
                          .col-12
                            p.mb-0 &lt;menu id=“file” value=“Archivo”&gt;
                          .col-12.mx-4
                            p.mb-0 &lt;popup&gt;
                          .col-12.mx-5  
                            p.mb-0 &lt;menuitem value=“Nuevo” onclick=“CreateNewDoc()”/&gt;
                          .col-12.mx-5  
                            p.mb-0 &lt;menuitem value=“Abrir” onclick=“OpenDoc()” /&gt;
                          .col-12.mx-5  
                            p.mb-0 &lt;menuitem value=“Cerrar” onclick=“CloseDoc()” /&gt;
                          .col-12.mx-5  
                            p.mb-0 &lt;menuitem value=“Guardar” onclick=“SaveDoc()” /&gt;
                          .col-12.mx-4
                            p.mb-0 &lt;/popup&gt;
                          .col-12
                            p.mb-0 &lt;/menu&gt;
                td.p-4 
                  .row
                    .col-12
                      .row.rounded.bg-gris.py-5.px-3.font-console
                        .col-12
                          p.mb-0 {
                        .col-12.mx-4
                          p.mb-0 "menu": {
                        .col-12.mx-5  
                          p.mb-0 "id": "file",
                        .col-12.mx-5  
                          p.mb-0 "value": "Archivo",
                        .col-12.mx-5  
                          p.mb-0 "popup": {
                        .col-11.offset-1.px-4 
                          p.mb-0.px-3 "menuitems": [
                        .col-10.offset-2.px-3 
                          p.mb-0 {
                        .col-10.offset-2.px-4 
                          p.mb-0.px-3 “value”: “Nuevo”,
                        .col-10.offset-2.px-4 
                          p.mb-0.px-3 “onclick”: “CreateNewDoc()”                          
                        .col-10.offset-2.px-3 
                          p.mb-0 },
                        .col-10.offset-2.px-3 
                          p.mb-0 {
                        .col-10.offset-2.px-4 
                          p.mb-0.px-3 “value”: “Abrir”,
                        .col-10.offset-2.px-4 
                          p.mb-0.px-3 “onclick”: “OpenDoc()”
                        .col-10.offset-2.px-3 
                          p.mb-0 },
                        .col-10.offset-2.px-3 
                          p.mb-0 {
                        .col-10.offset-2.px-4 
                          p.mb-0.px-3 “value”: "Cerrar”,
                        .col-10.offset-2.px-4 
                          p.mb-0.px-3 “onclick”: “CloseDoc()”
                        .col-10.offset-2.px-3 
                          p.mb-0 },
                        .col-10.offset-2.px-3 
                          p.mb-0 {
                        .col-10.offset-2.px-4 
                          p.mb-0.px-3 “value”: "Guardar”,
                        .col-10.offset-2.px-4 
                          p.mb-0.px-3 “onclick”: “SaveDoc()”
                        .col-10.offset-2.px-3 
                          p.mb-0 }
                        .col-11.offset-1.px-4 
                          p.mb-0.px-3 ]
                        .col-12.mx-5  
                          p.mb-0 }
                        .col-12.mx-4
                          p.mb-0 }
                        .col-12
                          p.mb-0 }
    .h4.mt-5 Bases de datos orientada a grafos
    p.mt-5 Un grafo es una colección de elementos (“nodos”) que aportan información, relacionados mediante “aristas”, que son la conexión entre los nodos, y que pueden tener una dirección concreta (Macarrón, 2021).
    .row.mt-5 
      .col-12.col-lg-10.col-xl-8.offset-lg-1.offset-xl-2
        .h4 Figura 4
        p.mt-4 Grafos
        figure.mt-4
          img(src="@/assets/template/tema1-15.png", alt="Texto que describa la imagen")
        figcaption.mt-4 Nota. Tomada de Macarrón (2021) 
    .row.mt-5
      .col-10.offset-1
        .tarjeta-avatar-b.mb-5
          img(src='@/assets/template/tema1-16.svg' alt='Texto que describa la imagen').w-15
          .tarjeta.bg-amarillo-claro
            .p-4
              p Este es un tipo de base de datos muy diferente a los anteriores; maneja la información de una manera particular, empleando grafos y teoría de grafos. Cada nodo solo debe contener una sola columna, entonces se deben normalizar completamente las bases de datos. Y solo aplica para grafos de tipo binario; cada nodo sólo se puede relacionar con otros dos nodos como máximo. Las ventajas de este tipo de bases de datos van enfocadas a la integridad de los datos y la optimización de consultas.
    .titulo-segundo.mt-5
      #t_1_4.h4 1.4  Sistemas de Gestión de Bases de Datos (SGBD) NoSQL
    .row.mt-3
      .col-2.col-lg-1.offset-5.offset-lg-0.align-self-center
        figure
          img(src="@/assets/template/tema1-17.svg" alt="Texto que describa la imagen")
      .col-12.col-lg-11.align-self-center.mt-3.mt-lg-0
        p Como se sabe, la base de datos sólo sirve si existe un sistema que la gestione, un SGBD. En NoSQL, hay varios SGBD y la mayoría son de código libre o libre distribución. A continuación, se muestran algunas de ellas, las más populares, con sus respectivas características. Es necesario tener en cuenta que, no obstante, pueden existir otros SGBD menos populares pero que pueden ser una buena opción en el momento de trabajar para Big Data. 
    .h4.mt-4 Tabla 5
    p.mt-4 Sistemas de gestión de bases de datos      
    .row.mt-5
      .col-6.col-lg-4.mt-3
        figure
          img(src="@/assets/template/tema1-18.png" alt="Texto que describa la imagen")
      .col-6.col-lg-4.mt-3
        figure
          img(src="@/assets/template/tema1-19.png" alt="Texto que describa la imagen")
      .col-6.col-lg-4.mt-3
        figure
          img(src="@/assets/template/tema1-20.png" alt="Texto que describa la imagen")
      .col-6.col-lg-4.mt-3
        figure
          img(src="@/assets/template/tema1-21.png" alt="Texto que describa la imagen")
      .col-6.col-lg-4.mt-3
        figure
          img(src="@/assets/template/tema1-22.png" alt="Texto que describa la imagen")
      .col-6.col-lg-4.mt-3
        figure
          img(src="@/assets/template/tema1-23.png" alt="Texto que describa la imagen")
      .col-6.col-lg-4.mt-3
        figure
          img(src="@/assets/template/tema1-24.png" alt="Texto que describa la imagen")
      .col-6.col-lg-4.mt-3
        figure
          img(src="@/assets/template/tema1-25.png" alt="Texto que describa la imagen")
      .col-6.col-lg-4.mt-3.offset-3.offset-lg-0
        figure
          img(src="@/assets/template/tema1-26.png" alt="Texto que describa la imagen")






</template>

<script>
export default {
  name: 'Tema1',
  components: {},
  data: () => ({}),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
}
</script>

<style lang="sass" scoped></style>
