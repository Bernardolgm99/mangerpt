<script setup>
import NavBar from '../components/NavBar.vue'
</script>

<template>
  <NavBar />


  <!-- Section 1 -->
  <header>
    <div class="section1">
      <h1 class="f-white"><span class="f-gigant">“</span>Uma experiência gastronómica que vai mudar sua vida<span
          class="f-gigant">”</span></h1>
    </div>
  </header>


  <!-- Section 2 -->
  <div>
    <v-row class="section2">
      <v-col class="d-flex justify-end pa-0">
        <div>
          <v-img :width="600" :height="512" aspect-ratio="16/9" src="../src/assets/images/chef.png"></v-img>
        </div>
      </v-col>
      <v-col class="text d-flex justify-start align-center">
        <p class="ms-16">
          Eu sou Manuel Brito Junior tenho 50 anos e sou chef de cozinha mas prefiro dizer que sou cozinheiro, não por
          humildade ou modéstia, mas por gostar de cozinhar e estar no calor e no stress de uma cozinha full time ao invés
          de passar mais tempo em um escritório, organizando e administrando, trabalho muito importante e essencial ,
          diga-se de passagem.
        </p>
      </v-col>
    </v-row>
  </div>


  <!-- Section 3 -->
  <div>
    <div class="section3 text d-flex justify-center align-center">
      <p class="drop-cap">
        Eu sempre cozinhei e gostei de estar na cozinha mas achava que era um hobby, até ser convidado para meu primeiro
        trabalho numa cozinha profissional em um restaurante no Algarve- Portugal. Foi quando tudo mudou e percebi que era
        isso que eu queria fazer para sempre e onde eu queria estar, numa cozinha, mas ao mesmo tempo vi que necessitava
        de conhecimento, pois o que eu sabia não era suficiente para me tornar um cozinheiro profissional então decidi me
        mudar para Londres e estudar no Le Cordon Bleu onde me formei no curso de cozinha e depois no de Patissiere.
      </p>
    </div>
  </div>

  <!-- Section 4 -->
  <div>
    <div>
      <h2>JOBS</h2>
      <div>
        <div></div>
        <div></div>
        <div></div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.drop-cap::first-letter {
  -webkit-initial-letter: 2;
          initial-letter: 2;
  color: rgb(216, 56, 56);
  font-weight: bold;
  margin-right: .25em;
}

header {
  height: 632px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-image: linear-gradient(to right, RGBA(0, 0, 0, .7), RGBA(0, 0, 0, .7)), url('../src/assets/images/header.png');
  background-position: center;
  background-size: cover;
}

.section1 {
  max-width: 450px;
}

.section2 {
  height: 512px;
  margin: 0px;
}

.section2 .text {
  background-color: #DA6852;
}

.section2 .text p {
  width: 400px;
}

.section3 {
  background-image: linear-gradient(to right, RGBA(0, 0, 0, .9), RGBA(0, 0, 0, .9)), url('../src/assets/images/section3.png');
  background-size: cover;
  background-position: center;
  height: 600px;
}

.section3 p {
  max-width: 1042px;
}

.text p {
  font-size: 24px;
  color: #e3e3e3;
}</style>
