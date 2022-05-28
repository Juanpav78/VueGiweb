
<template>
    <!--HTML EN VUE-->
  <div>
    <header>
      <h1 class="logo">{{logoText}}</h1>
      <img src="../src/assets/logo.png" alt="Logo Vue">
    </header>
    <section class="section1">
      <img src="../src/assets/logo.png" alt="Logo Vue">
      <img src="../src/assets/logo.png" alt="Logo Vue">
      <img src="../src/assets/logo.png" alt="Logo Vue">
    </section>
    <main>
      <div class="titulo">
        <h2 v-text="vText1"></h2>
      </div>
      
      <p v-html="textoHtml"> </p>
      <input class="button" type="button" href="www.google.com" v-model="inputText">
    </main>
    <footer>

    </footer>
    
    
  </div>
</template>
<script>


export default {
  //JAVASCRIPT EN VUE
 name: "App",
 data(){
   return {
     //Logo
      logoText: "Vue.JS",
      /* logoImg: "require('../src/assets/logo.png')",  PREGUNTAR*/
     //Texto
     vText1: "Hola mundo! Bienvenido a mi primera pagina web con VUE.JS",
     //Imagenes
     //Rutas
     
     
     textoHtml: '<a class="button" href="https://pandaxportfolio.netlify.app/" target="_blank"> ir alla</a>',
     inputText: "Escibe un texto" ,

   }
 },
}
</script>




<style>
/*CSS EN VUE */
/*Fuentes */
@import url('https://fonts.googleapis.com/css2?family=Comfortaa:wght@400;600;700&family=Indie+Flower&family=Pacifico&display=swap');/*Estilos */
html {
    font-size: 62.5%;
    box-sizing: border-box;
    
}
*, *:before, *:after {
    box-sizing: inherit;
}
body {
    font-size: 1.6rem;
    line-height: 1.8;
    background-color: #34495E;
    
}

h1, h2, h2{
  font-family: 'Pacifico', cursive;
  
}

.logo{
  color: #41B883;
  text-shadow: 0 -.5rem #34495E,
                0 0px 10px #000;
}

p, a{
  font-family: 'Comfortaa', cursive;
}

header, footer{
  background: rgb(63, 63, 63);
  height: 10rem;
}
header{
  position: relative;

  display: flex;
  flex-direction: row-reverse;
  justify-content: center;
  align-items: center;
  box-shadow: 0 0.5rem 11px 2px #111111;
}
header img{
  width: 5rem;
  height: 5rem;
}
.section1{
  background: azure;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  justify-items: center;

}

.titulo{
  width: 100%;
  text-align: center;
}
.titulo h2{
  font-family: 'Comfortaa', cursive;
  color: azure;
}
.button{

  padding: 1rem 2rem;
  background: azure;
  border-radius: 5px;
  text-decoration: none;
  color: #34495E;
  font-weight: 700;
  font-size: 2.4rem;
  border: 1.5px solid #41B883;
}
.button:hover{
  background: #41B883;
  
}
</style>
