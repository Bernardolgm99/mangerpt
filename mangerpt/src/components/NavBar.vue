<template>
  <nav class="conteiner">
    <v-container class="pa-0">
      <v-row class="ma-0">
        <v-col class="d-md-none"></v-col>
        <v-col class="d-flex justify-center pa-0">
          <div>
            <v-img class='pointer' :width="60" aspect-ratio="4/3" cover src="../src/assets/images/hat 1.png"></v-img>
          </div>
        </v-col>
        <v-col class="d-none d-md-block pa-0">
          <div class="d-flex justify-space-between h-100">
            <div class="navegationBtn pointer py-3 px-4">home</div>
            <div class="navegationBtn pointer py-3 px-4">menu</div>
            <div class="navegationBtn pointer py-3 px-4">contact</div>
          </div>
        </v-col>
        <v-col class="d-none d-md-block"></v-col>
        <v-col class="d-md-none d-flex justify-right"><button>menu</button></v-col>
      </v-row>
    </v-container>
  </nav>
</template>

<script setup>
</script>

<style scoped>
.navegationBtn {
  font-size: 18px;
}

.navegationBtn:hover {
  background-color:rgb(252, 76, 45);
  text-justify: center;
}
.pointer {
  cursor: pointer;
  -webkit-user-select: none;
  /* Safari */
  -ms-user-select: none;
  /* IE 10 and IE 11 */
  user-select: none;
  /* Standard syntax */
}
</style>

