
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
    <main :class="cont">
      <div class="titulo">
        <h2 v-text="vText1"></h2>
      </div>
      <div class="info">
        <p v-text="lorem"></p>
        <p v-text="lorem"></p>
        <p v-text="lorem"></p>

      </div>
      <div class="imagenes">
      <img :src="img1">
      <img :src="img2">
      <img :src="img3">
      </div>
      <p v-text="lorem"></p>
      <p v-text="lorem"></p>
      <div class="contain2"> 

        <div class="carta">
          <img :src="img4" alt="">
          <p v-text="vText2"></p>
          <div v-html="buttonGit"></div>
        </div>

        <div class="carta">
          <img :src="img5" alt="">
          <p v-text="vText3"></p>
          <div v-html="buttonPic"></div>
        </div>

        <div class="carta">
          <img :src="img6" alt="">
          <p v-text="vText4"></p>
          <div v-html="buttonPorta"></div>
        </div>
      
      </div>
      
      <input class="button separador" v-model="inputEvent" type="text" @keypress="presionaTecla()">
      
      <section class="clase3 contenedor">
        <div :class="caja">
        <h3>{{contador}}</h3>
        <p>{{parrafo}}</p>
        </div>
        <div class="caja_control">

          <div class="caja_control_numeros">
            <button @click="decrecerContador()">-</button>
            <h3>Aumentar o disminuir numero</h3>
            
            <button @click="incrementarContador()">+</button>
          </div>
           <div class="caja_control_colores">
             <h3>Cambiar color</h3>
             <select :class="caja" v-model="colorContenedor" @change="cambiarColor()" name="" id="">
            <option value="--Selecione--">--Selecione--</option>
            <option value="caja verde">verde</option>
            <option value="caja azul">azul</option>
            <option value="caja rojo">rojo</option>
            </select> 
           </div> 
            <div class="caja_control_texto">
              <h3>Cambiar texto</h3>
              <form>
              <textarea name="" id="" cols="47" rows="5" v-model="inputForm"></textarea>
              <a class="button"  @click="enviarFormulario()">Enviar</a>
              </form>
            </div>
            
        </div>
      </section>


    
    
        

        
    </main>
    <footer>
      <p>© 2022 - Juan Alvarado </p>
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
     lorem:"Lorem ipsum dolor sit amet consectetur adipiscing elit ligula aliquam accumsan, odio curae ac primis aptent potenti ad et. A accumsan aliquam erat dapibus nulla varius convallis est velit nisi, cubilia inceptos auctor dignissim",
     vText1: "Hola mundo! Bienvenido a mi primera pagina web con VUE.JS",
     vText2:"Para ver mis github y mis otros proyectos" ,
     vText3:"Para ver más imagenes como estas gracias a Lorem Picsum" ,
     vText4:"Para ver mi portafolio aunque no este terminado" ,
     //Imagenes
     img1: "https://i.picsum.photos/id/1020/4288/2848.jpg?hmac=Jo3ofatg0fee3HGOliAIIkcg4KGXC8UOTO1dm5qIIPc",
     img2: "https://i.picsum.photos/id/1025/4951/3301.jpg?hmac=_aGh5AtoOChip_iaMo8ZvvytfEojcgqbCH7dzaz-H8Y",
     img3: "https://i.picsum.photos/id/1084/4579/3271.jpg?hmac=YblMazviSugJVfZsFPaFI_Vp6lBeQin62qpm8rxHruo",
     img4: "https://i.picsum.photos/id/1042/3456/5184.jpg?hmac=5xr8Veg2D_kEQQO6rvGj_Yk8s_N4iq3-eZ9_KclSXNQ",
     img5: "https://i.picsum.photos/id/103/2592/1936.jpg?hmac=aC1FT3vX9bCVMIT-KXjHLhP6vImAcsyGCH49vVkAjPQ",
     img6: "https://i.picsum.photos/id/1035/5854/3903.jpg?hmac=DV0AS2MyjW6ddofvSIU9TVjj1kewfh7J3WEOvflY8TM",
     //Rutas
     buttonPorta:'<a class="button" href="https://pandaxportfolio.netlify.app/" target="_blank"> Portafolio</a>',
     buttonGit:'<a class="button" href="https://github.com/Juanpav78/" target="_blank"> Github </a>',
     buttonPic:'<a class="button" href="https://picsum.photos/" target="_blank"> Lorem Picsum </a>',
     inputText: "Escibe un texto" ,
     //Variables
     cont: "contenedor",
     //CONTADOR
     contador: 0,
     inputEvent: "" ,
     inputForm: "" ,
     parrafo: "Lorem ipsum dolor sit amet consectetur adipiscing elit ligula aliquam accumsan, odio curae ac primis aptent potenti ad et. A accumsan aliquam erat dapibus nulla varius convallis est velit nisi, cubilia inceptos auctor dignissim",
     caja:"caja",
     colorContenedor: "--Selecione--",
   }
 },
  methods: {
    incrementarContador(){
      this.contador++;
    },
    decrecerContador(){
      this.contador--;
    },
    presionaTecla(){
      alert(this.inputEvent);
    },
    cambiarColor(){
      this.caja = this.colorContenedor;
    },
    enviarFormulario(){
       this.parrafo = this.inputForm;
    },
    },
}
</script>




<style>
/*CSS EN VUE */
/*Colores*/

.verde{
  background: #41B883;
}

.gris{
  background: #34495E;
}

.rojo{
  background: #8d2929
}

.azul{
  background: #0e4881
}
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


h1, h2, h3{
  font-family: 'Pacifico', cursive;
  
}

.logo{
  color: #41B883;
  text-shadow: 0 -.5rem #34495E,
                0 0px 10px #000;
}

p, a{
  font-family: 'Comfortaa', cursive;
  color: azure;
  font-size: 1.8rem;
  font-weight: 600;
  text-align: justify;
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
.section1, .imagenes, .contain2{
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  justify-items: center;
}

.section1, .carta{
  background: azure;
  


}
.section1 img{
  max-width: 20rem;
  max-height: 20rem;
  width: 100%;
  height: 100%;
}
.contenedor{
  max-width: 120rem;
  margin: 0 auto;
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
  display: block;
  width: 100%;
  padding: 1rem 2rem;
  background: rgb(63, 63, 63);
  text-decoration: none;
  color: #34495E;
  font-weight: 700;
  font-size: 2.4rem;
  color: azure;
  text-align: center;
}
.button:hover{
  background: #41B883;
  color: #34495E;
  
}

.imagenes img, .carta img{
  max-width: 39rem;
  max-height: 26rem;
  width: 100%;
  height: 100%;
}
.imagenes img:hover{
  filter: blur(2px);
}

.contain2{
  gap: 2rem;
}

.carta{
  height: 42rem;
  
}
.carta p{
  color: #111111;
  width: 80%;
  margin: 0 auto;
  margin-bottom: .5rem;
  text-align: justify;
  height: 9.5rem;
  
}
.separador{
  margin: 4rem auto 3rem auto;
}

footer{
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}


.clase3{
  display: flex;
  justify-content: space-around;
  gap: 2rem;
  margin-bottom: 2rem;
  align-items: center;
}

.clase3 div{
  flex: 1;
  height: 35rem;
  max-height: 35rem;
  max-width: 40rem;
}

.clase3 .caja:first-child{
    display: flex;
    justify-content: center;
    align-items: center;
    border: dashed 3px #111111;
    flex-direction: column;
    padding: 2.4rem;
    
}

.caja_control{
  display: flex;
  flex-direction: column;
  background: rgb(63, 63, 63);
  
}

.caja_control .caja_control_numeros{
  display: flex;
  justify-content: space-between;
  padding: .5rem 1rem;
}
.caja_control .caja_control_numeros button{
  width: 3rem;
  height: 3rem;
  background: azure;
  border: none;
  box-shadow: inset 0 0 3px;
  border-radius: 3px;
  font-family: 'Comfortaa', cursive;
  font-weight: 600;
}
.caja_control h3{
  font-family: 'Comfortaa', cursive;
  margin: 0;
  font-weight: 400;
  text-align: center;
  text-decoration: underline 2px #41B883;
  color: azure;
}
.caja_control .caja_control_colores select{
  width: 100%;
  height: 3.5rem;
  text-align: center;
  font-family: 'Comfortaa', cursive;
}
.caja_control .caja_control_texto .button{
  border-top: solid 2px #41B883;
}

textarea{
  width: 100%;
}

@media (max-width: 1000px) {
 .imagenes img, .carta img{
  max-width: none;
  max-height: 25rem;
  width: 100%;
  height: 100%;
}
.imagenes, .contain2{
  grid-template-columns: repeat(1, 1fr);
  gap: 1rem;

}
.carta{
  margin-top:3rem ;
  height: 40rem;
  width: 90%;
  max-width: 50rem;
}
.imagenes img{
  margin:  auto;
  width: 90%;
  max-height: 40rem;
}

}
@media (max-width: 600px) {
 .imagenes img, .carta img{

  max-height: 26rem;
}


.imagenes img{
  margin:  auto;
  width: 90%;
}
.clase3{
  flex-direction: column;
  
}
}
</style>
