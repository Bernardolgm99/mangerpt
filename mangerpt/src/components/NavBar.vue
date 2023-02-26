<template>
  <nav class="conteiner">
    <v-row class="pt-2">
      <v-col class="d-md-none"></v-col>
      <v-col class="d-flex justify-center">
        <div>
          <v-img :width="50" aspect-ratio="16/9" src="../src/assets/images/hat 1.png"></v-img>
        </div>
      </v-col>
      <v-col class="d-none d-md-block pt-5">
        <div class="d-flex justify-space-between">
          <div class="navegationBtn">home</div>
          <div class="navegationBtn">menu</div>
          <div class="navegationBtn">contact</div>
        </div>
      </v-col>
      <v-col class="d-none d-md-block"></v-col>
      <v-col class="d-md-none d-flex justify-center"><button>menu</button>></v-col>
    </v-row>
  </nav>
</template>

<script setup>
</script>

<style scoped>
.navegationBtn {
  font-size: 18px;
}

.navegationBtn {
  font-weight: 100;
}
</style>
