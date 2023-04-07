<script setup>
import NavBar from '../components/NavBar.vue'
import Contact from '../components/Contact.vue'
import Gallery from '../components/Gallery.vue'
</script>

<template>
  <NavBar />

  <!-- Section 1 -->
  <header>
    <v-container class="section1">
      <img style="max-width: 100%; width: 521px; min-width: 100%; vertical-align: bottom;"
        src="/src/assets/icons/white-logo.png">
    </v-container>
  </header>


  <!-- Section 2 -->
  <div>
    <v-row class="section2 d-flex flex-wrap ma-0">
      <v-col class="d-flex justify-end pa-0 bg-white">
        <div class="chef-img" style="padding-right: 200px;">
          <img style="max-width: 100%; width: 521px; min-width: 100%; vertical-align: bottom;" src="/src/assets/icons/chef.jpg">
        </div>
      </v-col>
      <v-col class="text d-flex justify-start align-center pa-0">
        <p class=" ma-10">
          Eu sou Manuel Brito Junior tenho 50 anos e sou chef de cozinha, mas prefiro dizer que sou cozinheiro, não por
          humildade ou modéstia, mas por gostar de cozinhar e estar no calor e no stress de uma cozinha full time ao invés
          de passar mais tempo em um escritório, organizando e administrando, trabalho muito importante e essencial ,
          diga-se de passagem.
        </p>
      </v-col>
    </v-row>
  </div>


  <!-- Section 3 -->
  <div class="section3 d-flex justify-center align-center">
    <v-container>
      <div class="text d-flex justify-center align-center">
        <p class="drop-cap py-6">
          Eu sempre cozinhei e gostei de estar na cozinha mas achava que era um hobby, até ser convidado para meu primeiro
          trabalho numa cozinha profissional em um restaurante no Algarve- Portugal. Foi quando tudo mudou e percebi que
          era
          isso que eu queria fazer para sempre e onde eu queria estar, numa cozinha, mas ao mesmo tempo vi que necessitava
          de conhecimento, pois o que eu sabia não era suficiente para me tornar um cozinheiro profissional então decidi
          me
          mudar para Londres e estudar no Le Cordon Bleu onde me formei no curso de cozinha e depois no de Patissiere.
        </p>
      </div>
    </v-container>
  </div>

  <!-- Section 4 -->
  <div>
    <v-container class="d-flex align-center flex-column section4">
      <h2 class="mt-16 mb-5">JOBS</h2>
      <div class="d-flex justify-center flex-wrap w-100">
        <div class="mx-8 my-5 card-out d-flex justify-center align-center">
          <div class="card-in d-flex flex-column align-center text">
            <p class="my-auto mx-8">3 years St. Pancras Renaissance Hotel London</p><img class="mb-10"
              src="/src/assets/icons/stars.png">
          </div>
        </div>
        <div class="mx-8 my-5 card-out d-flex justify-center align-center">
          <div class="card-in d-flex flex-column align-center text">
            <p class="my-auto mx-8">1 year Grain Store London
            </p><img class="mb-10" src="/src/assets/icons/stars.png">
          </div>
        </div>
        <div class="mx-8 my-5 card-out d-flex justify-center align-center">
          <div class="card-in d-flex flex-column align-center text">
            <p class="my-auto mx-8">7 Years Hotel Union Øye Norway</p><img class="mb-10"
              src="/src/assets/icons/stars.png">
          </div>
        </div>
      </div>
      <p class="my-16">“Me considero muito profissional e exigente, prezo muito pela qualidade e sabor. Só uso
        ingredientes
        de primeira qualidade, pois acredito que é a base de tudo. Posso dizer que sou bem Old School.”</p>
    </v-container>
  </div>

  <!-- Section 5 -->
  <div class="bg-black">
    <v-container class="text py-16">
      <p>A ideia do <span style="font:arial; color: rgb(216, 56, 56); font-size: 35px;">manger.pt</span> surgiu na vontade
        e na necessidade de fazer parte de um novo mercado e também me desafiar noutras andanças, como esse mundo digital,
        dando a conhecer minhas delícias e trabalho e também minha fascinação pela cozinha.</p>
    </v-container>
  </div>

  <!-- Section 6 -->
  <div class="section6">
    <v-container class="d-flex justify-center py-16">
      <div class="card-menu d-flex flex-column align-center justify-space-between">
        <h3 class="mb-6">MENU</h3>
        <p class="mb-16">Serão inicialmente 7 sobremesas e um Pão na nossa loja , mas sempre com a possibilidade de
          aceitar qualquer
          encomenda, doce ou salgada, mediante consulta, posso garantir que serão de altíssima qualidade e
          com muito sabor.</p>
        <button class="pointer" @click="goMenu">Go to menu</button>
      </div>
    </v-container>
  </div>

  <Gallery />

  <Contact />
</template>

<script>
export default {
  methods: {
    goMenu() {
      window.scrollTo(0, 0);
      this.$router.push({ name: 'menu' });
    },
    components: { Gallery }
  }
}
</script>

<style scoped>
h2 {
  font-size: 40px;
  font-weight: 500;
}

.drop-cap::first-letter {
  -webkit-initial-letter: 3;
  initial-letter: 3;
  color: rgb(216, 56, 56);
  font-weight: bold;
  margin-right: .25em;
}

.card-out {
  background-color: #111111;
  min-height: 400px;
  min-width: 320px;
}

.card-in {
  border: 3px solid #e3e3e3;
  height: 380px;
  width: 300px;
  text-align: center;
}

header {
  height: 632px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-image: linear-gradient(to right, RGBA(0, 0, 0, .7), RGBA(0, 0, 0, .7)), url('/src/assets/icons/section2.jpg');
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
}

.section1 {
  max-width: 500px;
}

.section2 .text {
  background-color: #DA6852;
}

.section2 .text p {
  width: 500px;
}

.chef-img {
  padding-right: 200px;
}

@media screen and (max-width:1100px) {

  .chef-img {
    padding-right: 0px;
  }
  .section2 {
    flex-direction: column;
  }

  .section2 div {
    justify-content: center !important;
  }

  .section2 .text p {
    width: 75vw;
    margin-left: auto;
    margin-right: auto;
  }
}

.section3 {
  background-image: linear-gradient(to bottom, RGBA(0, 0, 0, .9), RGBA(0, 0, 0, .8)), url('/src/assets/icons/hat2.png');
  background-size: contain;
  background-position: center;
  background-attachment: fixed;
  min-height: 350px;
}

.section3 p {
  width: 75vw;
}

.section4 p {
  font-size: 24px;
}

.text p {
  font-size: 24px;
  color: #e3e3e3;
}

.section6 {
  background-image: linear-gradient(to right, RGBA(0, 0, 0, .7), RGBA(0, 0, 0, .7)), url('/src/assets/icons/section1.jpg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
}

.card-menu {
  max-width: 600px;
  background-color: #010101;
  color: #e3e3e3;
  padding: 50px 100px 100px 100px;
  text-align: center;
}

@media screen and (max-width:960px) {
  .section3 p {
    max-width: 100vw;
  }

  .card-menu {
    padding: 50px 50px 100px 50px;
  }
}

h3 {
  font-size: 40px;
}

.card-menu p {
  font-size: 24px;
}

.card-menu button {
  font-size: 24px;
  border: 1px solid #e3e3e3;
  padding: 10px 50px
}

.card-menu button:hover {
  background-color: #111
}

.card-menu button:active {
  background-color: #333;
}

.pointer {
  cursor: pointer;
  -webkit-user-select: none;
  /* Safari */
  -ms-user-select: none;
  /* IE 10 and IE 11 */
  user-select: none;
  /* Standard syntax */
}</style>