<template>
  <div>
    <h1>{{mensaje}}</h1>
    <h2 v-text="texto"></h2>
    <p v-html="textoHtml"> </p>
    <input type="text" v-model="inputText">
  </div>
</template>
<script>
export default {
 name: "App",
 data(){
   return {
     mensaje: "Holaa",
     texto: "Hola mundo!",
     textoHtml: '<a href="https://www.google.com/webhp?hl=es&sa=X&ved=0ahUKEwj9w8jAr_73AhUYp3IEHcHiCHkQPAgI" target="_blank"> ola</a>',
     inputText: "Escibe un texto" ,
   }
 },
}
</script>




<style>
html{
  height: 100%;
}
body{
  background-image: linear-gradient(0deg, rgba(7,180,145,0.8491879350348028) 0%, rgba(9,121,116,1) 31%, rgba(2,195,229,1) 75%, rgba(0,212,255,1) 100%);
  height: 100%;
}
</style>
