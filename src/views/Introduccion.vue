<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
  
    .titulo-principal
      .titulo-principal__numero
        span
          i.fas.fa-info
      h1 Introducción
    figure
      img(src="@/assets/template/tema-0-1.png", alt="Texto que describa la imagen")
    .row.mt-4
      .col-12.col-lg-9
        p El almacenamiento de información es importante en las empresas ya integradas en la era digital, debido a que se dispone de una cantidad significativa de datos. Los especialistas en análisis de datos elaboran estrategias que pueden ayudar a identificar mejor las necesidades de clientes y prever riesgos o el comportamiento del mercado. Es por esto que las empresas saben de la importancia de administrar tanta información de sus clientes y del mercado. Por tanto, aparecen nuevas necesidades para las cuales el Big Data, que hace referencia a la administración de enormes volúmenes de datos, enfoca sus esfuerzos en procesar información con características de gran volumen, dejando de lado otros aspectos de los datos que, en el caso de las bases de datos tradicionales, se concentran más en la integridad o la no repetición de los datos.
        p.mt-3 Para la elaboración de este componente, se abordaron varios autores conocidos en bases de datos NoSQL, de quienes se han citado y referenciado conceptos y ejemplos para los fines educativos de esta materia, en el entendido que el conocimiento es social y, por lo tanto, es para usarlo por quienes necesitan adquirirlo. Se espera que este documento sea útil para todos, aprendices y lectores en general, que estén interesados en acercarse a asuntos básicos de la programación de aplicaciones y servicios para la nube.
      .col-4.col-lg-3.offset-4.offset-lg-0.align-self-center
        figure
          img(src="@/assets/template/tema-0-2.svg", alt="Texto que describa la imagen")
</template>

<script>
export default {
  name: 'Introduccion',
  data: () => ({
    // variables de vue
  }),
}
</script>

<style lang="sass" scoped>
.introduccion
</style>
