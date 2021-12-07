<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5
    .titulo-principal
      .titulo-principal__numero
        span 3
      h1 Manipulación de datos con MongoDB
    .row
      .col-10.offset-1
        .bloque-texto-a.color-acento-botones.p-4.p-md-5.mb-5 
          .row.m-0.align-items-center.justify-content-between
            .col-lg-8
              .bloque-texto-a__texto.p-4
                p Las bases de datos deben poder manipular la información de varias maneras, ya que los procesos en los sistemas informáticos necesitan de esas operaciones básicas, tales como crear datos, consultarlos, actualizarlos y, en algún punto, eliminarlos. #[strong (Create, Read, Update and Delete - CRUD).]
                p.mt-3 Por tanto, queda establecido que almacenarla o contenerla no es su mera y única función básica. 
            .col-lg-4.mb-4.mb-lg-0
              figure
                img(src="@/assets/template/tema3-1.svg", alt="Texto que describa la imagen") 
    .titulo-segundo.mt-5
      #t_3_1.h4 3.1  Crear documentos
    figure.mt-4
      img(src="@/assets/template/tema3-2.png", alt="Texto que describa la imagen")
    p.mt-5 Es la primera de cuatro funciones elementales a la hora de utilizar bases de datos. Crear documentos permite insertar unidades de información; en el caso de MongoDB, a través de documentos en colecciones de datos.
    AcordionA.mb-5(tipo="b" clase-tarjeta="tarjeta bg-gris").mt-4
      .row(titulo="Para crear un documento")
        p Para poder crear un documento, MongoDB posee el método .insert(), #[strong .save()] y, de una manera especial, #[strong .update()] #[strong .(Graterol, 2014).]
        .row 
          .col-12
            .row.rounded.bg-gris-oscuro.p-5.font-console
              .col-12
                p.mb-0 &lt;documento = {
              .col-12
                p.mx-4.mb-0 “titulo” : “Titulo Libro”,
              .col-12
                p.mx-4.mb-0 “Autores” : [“Peter”,”Johnathan”]
              .col-12
                p.mb-0 }
              .col-12
                p.mb-0 { “titulo” : “Titulo Libro”, “Autores” : [ “Peter”, “Johnathan” ] }&gt;
              .col-12
                p.mb-0 &lt;db.libros.insert(documento)WriteResult({ “nInserted” : 1 })&gt;
              

      div(titulo="Insertar varios simultáneamente")
        p Se pueden insertar varios a la vez:
        .row 
          .col-12
            .row.rounded.bg-gris-oscuro.p-5.font-console
              .col-12
                p.mb-0 &lt;documentos = [{
              .col-12
                p.mx-4.mb-0 “titulo” : “Otro Libro”,
              .col-12
                p.mx-4.mb-0 “Autores” : [“Peter”,“Yolima”]
              .col-12
                p.mx-4.mb-0 },
              .col-12
                p.mb-0.mx-4 {
              .col-12
                p.mx-4.mb-0 “titulo” : “Nuevo Libro”,
              .col-12
                p.mx-4.mb-0 “Autores” : [“Zulema”]
              .col-12
                p.mb-0 }]
              .col-12
                p.mb-0 [
              .col-12
                p.mx-4.mb-0 {
              .col-12
                p.mx-5.mb-0 “titulo” : Otro Libro”,
              .col-12
                p.mx-5.mb-0 “Autores” : [ “Peter”, “Yolima” ]
              .col-12
                p.mx-4.mb-0 },
              .col-12
                p.mx-4.mb-0 {
              .col-12
                p.mx-5.mb-0 “titulo” : “Nuevo Libro”,
              .col-12
                p.mx-5.mb-0 “Autores” : [ “Zulema” ]
              .col-12
                p.mx-4.mb-0 }
              .col-12
                p.mb-0 ]
              .col-12
                p.mb-0 &lt;db.libros.insert(documentos) = [{
              .col-12
                p.mx-1.mb-0 BulkWriteResult({
              .col-12
                p.mx-5.mb-0 “writeErrors” : [ ],
              .col-12
                p.mx-5.mb-0 “writeConcernErrors” : [ ],
              .col-12
                p.mx-5.mb-0 “nInserted” : 2,
              .col-12
                p.mx-5.mb-0 “nUpserted” : 0,
              .col-12
                p.mx-5.mb-0 “nMatched” : 0,
              .col-12
                p.mx-5.mb-0 “nModified” : 0,
              .col-12
                p.mx-5.mb-0 “nRemoved” : 0,
              .col-12
                p.mx-5.mb-0 “upserted” : [ ]
              .col-12
                p.mx-4.mb-0 })
                .col-12
                p.mb-0 &gt;
      div(titulo="Actualizar documento")
        p Tiene todas las funciones de .insert(), pero además permite actualizar un documento si ya existe el _id de dicho documento. En ese caso, .insert() mostraría una excepción.
        figure.mt-4
          img(src="@/assets/template/tema3-3.png" , alt="Texto que describa la imagen")
      
    .titulo-segundo.mt-5
      #t_3_2.h4 3.2  Leer y consultar colecciones
    p.mt-5 Cuando de la función leer y consultar la información se trata, la forma básica consiste en usar el método find() de la colección, tal como ya se ha dicho en un punto anterior de este componente formativo.
    LineaTiempoD.color-acento-botones.mt-5
      .row(numero="1" titulo="Leer y consultar colecciones")
        .col-12.px-4
          .row.rounded.bg-gris-oscuro.p-5.font-console
            .col-12
              p.mb-0 &lt;db.libros.find()
            .col-12
              p.mx-4.mb-0 { “_id” : ObjectId(“60d159461e0ed70729ced13e”), “titulo” : “Titulo Libro”, “Autores” : [ “Peter”, “Johnathan” ] }
            .col-12
              p.mx-4.mb-0 { “_id” : ObjectId(“60d159df1e0ed70729ced13f”), “título” : “Otro Libro”, “Autores” : [ “Peter”, “Yolima” ] }
            .col-12
              p.mx-4.mb-0 { “_id” : ObjectId(“60d159df1e0ed70729ced140”), “título” : “Nuevo Libro”, “Autores” : [ “Zulema” ] }
            .col-12
              p.mb-0 &gt;
      .row(numero="2" titulo="Función pretty()")
        p Otra forma de mejor visualización es aplicar la función pretty().
        .col-12.px-4
          .row.rounded.bg-gris-oscuro.p-5.font-console
            .col-12
              p.mb-0 &lt;db.libros.find().pretty()
            .col-12
              p.mb-0 {
            .col-12
              p.mx-4.mb-0 “_id” : ObjectId(“60d159461e0ed70729ced13e”),    
            .col-12
              p.mx-4.mb-0 “titulo” : “Titulo Libro”,
            .col-12
              p.mx-4.mb-0 “Autores” : [ “Peter”, “Johnathan” ]          
            .col-12 
              p.mb-0 }, 
            .col-12
              p.mb-0 {
            .col-12
              p.mx-4.mb-0 “_id” : ObjectId(“60d159df1e0ed70729ced13f”), 
            .col-12
              p.mx-4.mb-0 “título” : “Otro Libro”,
            .col-12
              p.mx-4.mb-0 “Autores” : [ “Peter”, “Yolima” ]          
            .col-12 
              p.mb-0 },
            .col-12
              p.mb-0 {
            .col-12
              p.mx-4.mb-0 “_id” : ObjectId(“60d159df1e0ed70729ced140”), 
            .col-12
              p.mx-4.mb-0 “título” : “Nuevo Libro”,
            .col-12
              p.mx-4.mb-0 “Autores” : [ “Zulema” ]         
            .col-12 
              p.mb-0 } 
            .col-12
              p.mb-0 &gt;
    .titulo-segundo.mt-5
      #t_3_3.h4 3.3   Actualizar documentos
    .row.mt-5 
      .col-8.offset-2
        .cajon.color-primario.p-4.mb-4.bg-azul-claro
          .row
            .col-3.d-none.d-lg-block.align-self-center
              figure
                img(src="@/assets/template/tema3-4.svg" , alt="Texto que describa la imagen").w-75
            .col-12.col-lg-9
              p.mb-0 Es momento de ver un ejemplo de cómo se actualiza la información en la base de datos; ello, conociendo el contenido del atributo _id del documento a actualizar. Preste atención a la siguiente estructura: 
    .row.mx-0.mt-3
      .col-8.offset-2
        .row.rounded.bg-gris-oscuro.p-5.font-console
          .col-12
            p.mb-0 db.collection.update (
          .col-12
            p.mx-4.mb-0 &lt; consulta - criterios &gt;,
          .col-12
            p.mx-4.mb-0 &lt; documento modificado &gt;,
          .col-12
            p.mx-4.mb-0 {upsert: true | false, multi : true | false }
          .col-12
            p.mb-0 }
    .row.mt-5 
      .col-8.offset-2
        .cajon.color-primario.p-4.mb-4.bg-azul-claro
          .row 
            p La opción upsert, permite agregar un documento si no existe, siempre y cuando esta opción esté activada.
    .row.mx-0.mt-3
      .col-8.offset-2
        .row.rounded.bg-gris-oscuro.p-5.font-console
          .col-12
            p.mb-0 &gt; db.libros.update({“_id”: ObjectId(“60d159df1e0ed70729ced13f”) },{“titulo”:”Titulo Modificado”}) 
            p.mb-0 WriteResult({ “nMatched” : 1, “nUpserted” : 0, “nModified” : 1 }) 
            p &gt;
    .titulo-segundo.mt-5
      #t_3_4.h4 3.4   Borrar documentos   
    .row.mt-5 
      .col-8.offset-2
        .cajon.color-primario.p-4.mb-4.bg-azul-claro
          .row
            .col-3.d-none.d-lg-block.align-self-center
              figure
                img(src="@/assets/template/tema3-5.svg" , alt="Texto que describa la imagen").w-75
            .col-12.col-lg-9
              p.mb-0 El método remove() elimina uno o más documentos de una colección. Recibe parámetros para realizar una eliminación selectiva; si no se le pasa ningún parámetro, elimina todos los documentos de la colección #[strong (Graterol, 2014).] Esto nos conduce a concluir que las bases de datos #[strong no relacionales] son más sencillas de administrar, al no tener que hacer uso de estructuras complejas e interrelacionadas.
    .row.mx-0.mt-3
      .col-8.offset-2
        .row.rounded.bg-gris-oscuro.p-5.font-console
          .col-12
            p.mb-0 &lt;db.libros.remove({“_id”: ObjectId(“60d159df1e0ed70729ced13f”) }) WriteResult({ “nRemoved” : 1 }) 
            p &gt;
    .row.mt-5 
      .col-8.offset-2
        .cajon.color-primario.p-4.mb-4.bg-azul-claro
          .row 
            p La función .drop() elimina toda una colección y es la más recomendable a la hora de realizar esta tarea, ya que utiliza menos recursos que .remove(). #[strong (Yohan D, 2014).]
    .row.mx-0.mt-3
      .col-8.offset-2
        .row.rounded.bg-gris-oscuro.p-5.font-console
          .col-12
            p.mb-0 &gt; db.libros.drop(); 
            p.mb-0  true            
            p.mb-0 &gt; show collections
          .col-12
            p.mb-0 coleccion_personas 
            p.mb-0 &gt;



</template>

<script>
export default {
  name: 'Tema3',
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
