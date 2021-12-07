<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5
    .titulo-principal
      .titulo-principal__numero
        span 2
      h1 NoSQL con MongoDB.
    figure.mt-3
      img(src="@/assets/template/tema2-1.png" alt="Texto que describa la imagen")
    p.mt-5 Como se mencionó antes, MongoDB es un sistema de bases de datos no relacionales, multiplataforma, es decir, se puede instalar en cualquier sistema operativo para servidor (Windows, Linux, BSD, MAC). El tipo de base de datos empleada es el tipo de base de datos documental, pero también se pueden administrar bases de datos clave/valor. 
    .row.mt-5
      .col-8.offset-2
        .bloque-texto-g.color-primario.p-3.p-sm-4.p-md-5.mb-5
          .bloque-texto-g__img(
            :style="{'background-image': `url(${require('@/assets/template/tema2-2.png')})`}")
          .bloque-texto-g__texto.p-4
            p.mb-0 El tipo de licencia de software libre es, específicamente, GNU AGPL v3.0. MongoDB usa el formato BSON (JSON compilado) para guardar la información.
    .titulo-segundo.mt-5
      #t_2_1.h4 2.1  Conceptos básicos
    .row.mt-4
      .col-10.offset-1.borde-gris.rounded-25
        .row
          .col-4.px-0
            figure
              img(src="@/assets/template/tema2-3.png" alt="Texto que describa la imagen")
          .col-8.align-self-center
            p Los siguientes conceptos son claves para la asimilación de todos los elementos de este componente formativo. Para la implementación de bases de datos, conviene tener claridad acerca de lo que es un documento, una colección, a qué se hace referencia cuando se habla de creación y actualización de bases de datos, instalación de licencias, entre otros.
    .row.mt-5
      .col-
        //- LineaTiempoD debe ir acompañado de una de una de estas clases => 
        //- .color-primario, .color-secundario, .color-acento-contenido, .color-acento-botones
        LineaTiempoD.color-acento-botones
          p.text-small(numero="1" titulo="JSON – JavaScript Object Notation") Como la información gestionada usa el formato JSON para representar objetos según la especificación documento RFC 46274, y como JSON es independiente del lenguaje, se ha popularizado mucho el uso del lenguaje JavaScript. JSON es usado por muchos sistemas para intercambiar datos, por lo sencillo que es, si se compara con XML.

          p.text-small(numero="2" titulo="Documento") Un documento es un conjunto de datos estructurados, pero esta estructura no es estática, es decir, puede variar de un documento a otro. La estructura básica contiene pares clave/valor y se usa BSON (JSON Binario) como formato para almacenar los documentos dentro del SGBD. Un documento es como el equivalente a una fila dentro de una tabla de un modelo relacional.

          p.text-small(numero="3" titulo="Colección") En este contexto, cuando se habla de colección, se está haciendo referencia a un conjunto de documentos. Se puede asemejar a una tabla en las bases de datos relacionales.
    .titulo-segundo.mt-5
      #t_2_2.h4 2.2  Instalación de MongoDB
    figure.mt-4
      img(src="@/assets/template/tema2-4.png", alt="Texto que describa la imagen")
    p.mt-5 La instalación de MongoDB en un sistema Windows 10, comenzando por su descarga, implica el seguimiento de una serie de pasos ordenados. En este punto del contenido formativo, se dará a conocer el recorrido detallado para tal instalación. 
    p.mt-3 Siga cuidadosamente las instrucciones que se encuentran en el siguiente documento y luego aplíquelas en su computador. 
    p.mt-5 Visite
    .row.mt-4
      .col-8.col-lg-5
        a.anexo(href="https://www.mongodb.com/" target="_blank")
          .anexo__icono
            img(src="@/assets/template/icono-link.svg")
          .anexo__texto
            p #[strong Enlace web.] https://www.mongodb.com/
    p.mt-4 Estando allí, haga clic en Software y Community Server para aplicar los pasos:
    .row.mt-5
      .col-10.offset-1
        .tarjeta.color-primario.p-3.mb-5
          .row.justify-content-around.align-items-center
            .col-3.col-sm-2.col-lg-1
              img(src="@/assets/template/tema2-5.svg")
            .col
              .row.justify-content-between.align-items-center
                .col.mb-3.mb-sm-0
                  .row
                    .col-3.col-sm-2.col-lg-1
                      figure
                        img(src="@/assets/template/tema-2-6.svg")
                    .col.px-0.pt-3
                      p.texto-blanco Instalación de MongoDB
                .col-sm-auto
                  a.boton.color-acento-contenido.texto-blanco(:href="obtenerLink('/downloads/Instalacion_MongoDB.pdf')" target="_blank")
                    span Descargar
                    i.fas.fa-file-download
    .titulo-segundo.mt-5
      #t_2_3.h4 2.3 Consola interactiva
    figure.mt-4
      img(src="@/assets/template/tema2-7.png" , alt="Texto que describa la imagen")
    p.mt-5 MongoDB tiene, al igual que todas las bases de datos, una interfaz de línea de comando (CLI), desde la cual se puede acceder a un API de las funcionalidades. Podemos acceder a su consola interactiva y realizar nuestras primeras interacciones con MongoDB.
    AcordionA.mb-5(tipo="b" clase-tarjeta="tarjeta bg-gris")
      .row(titulo="Ingreso")
        p Para ingresar a su consola interactiva, hay que dirigirse a la carpeta donde quedó instalado MongoDB. (C:\Program Files\MongoDB\Server\4.4\bin). Se debe dar clic en el ejecutable que se llama mongo.exe, como se muestra aquí:
        .h4.mt-4 Figura 16
        p.mt-4 Consola interactiva
        figure.mt-4
          img(src="@/assets/template/tema2-8.png" , alt="Texto que describa la imagen")
      div(titulo="Instalación exitosa")
        p Si la vista es como se muestra a continuación, es porque la instalación fue exitosa.
        .h4.mt-4 Figura 17
        p.mt-4 Instalación exitosa
        figure.mt-4
          img(src="@/assets/template/tema2-9.png" , alt="Texto que describa la imagen")
      div(titulo="Prueba")
        p Para probar que está funcionando bien, se escribe el comando ‘help’.
        .h4.mt-4 Figura 18
        p.mt-4 Comprobación de funcionamiento
        figure.mt-3
          img(src="@/assets/template/tema2-10.png", alt="alt")
        //- .row.mt-4
        //-   .col-12
        //-     .row
        //-       .col-12.rounded-25.bg-gris-oscuro.py-5.px-3.font-console
        //-         .row.px-5
        //-           .col-4
        //-             .row
        //-               .col-12
        //-                 p.mb-0 &lt; help
        //-               .col-12.mx-5  
        //-                 p.mb-0 db.help()
        //-               .col-12.mx-5  
        //-                 p.mb-0 db.mycoll.help() 
        //-               .col-12.mx-5  
        //-                 p.mb-0 sh.help()
        //-               .col-12.mx-5  
        //-                 p.mb-0 rs.help()
        //-               .col-12.mx-5  
        //-                 p.mb-0 help admin
        //-               .col-12.mx-5  
        //-                 p.mb-0 help connect                 
        //-               .col-12.mx-5  
        //-                 p.mb-0 help keys                    
        //-               .col-12.mx-5  
        //-                 p.mb-0 help misc                    
        //-               .col-12.mx-5  
        //-                 p.mb-0 help mr                      
        //-               .col-12.mx-5.mt-3  
        //-                 p.mb-0 show dbs
        //-               .col-12.mx-5  
        //-                 p.mb-0 show collections             
        //-               .col-12.mx-5  
        //-                 p.mb-0 show users                   
        //-               .col-12.mx-5  
        //-                 p.mb-0 show profile                 
        //-               .col-12.mx-5  
        //-                 p.mb-0 show logs                    
        //-               .col-12.mx-5  
        //-                 p.mb-0 show log [name]              
        //-               .col-12.mx-5  
        //-                 p.mb-0 use &lt;db_name&gt;                
        //-               .col-12.mx-5  
        //-                 p.mb-0 db.mycoll.find()             
        //-               .col-12.mx-5  
        //-                 p.mb-0 db.mycoll.find( { a : 1 } )  
        //-               .col-12.mx-5  
        //-                 p.mb-0 it
        //-               .col-12.mx-5  
        //-                 p.mb-0 DBQuery.shellBatchSize = x   
        //-               .col-12.mx-5  
        //-                 p.mb-0 exit         
        //-               .col-12
        //-                 p.mb-0 &gt;                                      
        //-           .col-8
        //-             .row
        //-               .col-12
        //-                 p.mb-0 #[br]
        //-               .col-12  
        //-                 p.mb-0 help on db methods
        //-               .col-12  
        //-                 p.mb-0 help on collection methods
        //-               .col-12  
        //-                 p.mb-0 sharding helpers
        //-               .col-12  
        //-                 p.mb-0 replica set helpers
        //-               .col-12  
        //-                 p.mb-0 administrative help          
        //-               .col-12  
        //-                 p.mb-0 connecting to a db help          
        //-               .col-12  
        //-                 p.mb-0 key shortcuts      
        //-               .col-12  
        //-                 p.mb-0 misc things to know                
        //-               .col-12
        //-                 p.mb-0 mapreduce
        //-               .col-12.mt-3    
        //-                 p.mb-0 show database names           
        //-               .col-12  
        //-                 p.mb-0 show collections in current database         
        //-               .col-12  
        //-                 p.mb-0 show users in current database
        //-               .col-12  
        //-                 p.mb-0 show most recent system.profile entries with time &gt;= 1ms
        //-               .col-12  
        //-                 p.mb-0 show the accessible logger names
        //-               .col-12  
        //-                 p.mb-0 prints out the last segment of log in memory, ‘global’ is default              
        //-               .col-12  
        //-                 p.mb-0 set current database
        //-               .col-12  
        //-                 p.mb-0 list objects in collection mycoll  
        //-               .col-12  
        //-                 p.mb-0 list objects in mycoll where a == 1
        //-               .col-12  
        //-                 p.mb-0 result of the last line evaluated; use to further iterate
        //-               .col-12  
        //-                 p.mb-0 set default number of items to display on shell 
        //-               .col-12  
        //-                 p.mb-0 quit the mongo shell
                       
      div(titulo="Seleccionar base de datos")
        p Al igual que en bases de datos relacionales, se debe usar un comando para seleccionar una base de datos, pero antes de eso es necesario mirar qué bases de datos existen, con el siguiente comando:
        .h4.mt-4 Figura 19
        p.mt-4 Comando ‘show dbs’
        figure.mt-4
          img(src="@/assets/template/tema2-11.png" , alt="Texto que describa la imagen")
      div(titulo="Comando de selección")
        p El comando para seleccionar una base de datos es use &lt;nombre base de datos&gt;.
        .h4.mt-4 Figura 20
        p.mt-4 Nombre base de datos
        figure.mt-4
          img(src="@/assets/template/tema2-12.png" , alt="Texto que describa la imagen")
      div(titulo="Crear base de datos")
        p El comando #[strong use] se usa también para crear una nueva base de datos. El comando sería ‘use pruebas’:
        .h4.mt-4 Figura 21
        p.mt-4 Use pruebas
        figure.mt-4
          img(src="@/assets/template/tema2-13.png" , alt="Texto que describa la imagen")
        p.mt-3 El comando #[strong show dbs] no mostrará esta base de datos hasta que exista el primer documento. 
    .titulo-segundo.mt-5
      #t_2_4.h4 2.4  Crear primer documento
    .row.mt-4
      .col-10.offset-1.borde-gris.rounded-25
        .row
          .col-4.px-0
            figure
              img(src="@/assets/template/tema2-14.png" alt="Texto que describa la imagen")
          .col-8.align-self-center
            p Se creará una base de datos y una colección, y eso se hará almacenando un documento usando el objeto #[strong db], pero primero se debe ejecutar el comando #[strong use]. Un documento puede tener, en teoría, un máximo de hasta 16MB de información.
    .row.mt-5 
      .col-10.offset-1
        .cajon.color-primario.p-4.mb-4.bg-azul-claro
          p Aprovechando el primer objeto visto, JSON, para almacenarlo en MongoDB y consultarlo, se debe tener en cuenta, dentro de la consola interactiva, usar variables para crear o modificar documentos; de esta manera, se pueden evitar accidentes con una mala manipulación directa de la base de datos.
    .row.mt-5
      .col-10.offset-1
        .h4 Figura 22
        p.mt-4 Creación del primer documento
        figure.mt-4
          img(src="@/assets/template/tema2-15.png" , alt="Texto que describa la imagen")
    p.mt-5 Habría que añadir que, de esta manera, para almacenar un documento, es necesario ejecutar el método insert() del objeto #[strong db], especificando el nombre de la colección #[strong (la colección se crea de manera dinámica, como la base de datos).] 
    .row.mt-5
      .col-10.offset-1
        .h4 Ejemplo
        .h4.mt-4 Figura 23
        p.mt-4 Almacenar un documento
        figure.mt-4
          img(src="@/assets/template/tema2-17.png" , alt="Texto que describa la imagen")
    .h4.mt-5 Primera colección
    p.mt-5 Es así como se ha creado la primera colección de nombre #[strong coleccion_personas] y nuestro primer documento. Para confirmar esto, se puede ejecutar el comando #[strong show collections.]
    .row.mt-5
      .col-10.offset-1
        .h4.mt-4 Figura 24
        p.mt-4 Creación de una colección
        figure.mt-4
          img(src="@/assets/template/tema2-18.png" , alt="Texto que describa la imagen")
    .h4.mt-5 Método find()
    p.mt-5 Para consultar los documentos, se usa el método find() de la colocación, como se muestra a continuación: 
    .row.mt-5
      .col-10.offset-1
        .h4.mt-4 Figura 25
        p.mt-4 Consulta de documentos
        figure.mt-4
          img(src="@/assets/template/tema2-19.png" , alt="Texto que describa la imagen")
    .row.mt-5 
      .col-10.offset-1
        .cajon.color-acento-botones.p-4.mb-4.bg-amarillo-claro
          .row
            .col-2.d-none.d-lg-block
              figure
                img(src="@/assets/template/tema2-16.svg" , alt="Texto que describa la imagen")
            .col-12.col-lg-10
              .h4 Llave primaria
              p Note que existe un atributo que nunca se definió, llamado #[strong _id]. Este es un índice, que es lo equivalente a llave primaria.


</template>

<script>
export default {
  name: 'Tema2',
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
