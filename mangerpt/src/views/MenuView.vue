<script setup>
import NavBar from '../components/NavBar.vue'
import Contact from '../components/Contact.vue'
</script>

<template>
  <NavBar />
  <header class="d-flex justify-center align-center">
    <h1 class="f-white">Desserts & Salty</h1>
  </header>
  <div>
    <div class="section-menu">
      <v-container class="menu">
        <h2 class="ml-9 mb-9 f-white">Menu</h2>
        <div v-for="type in product_for_type" class="type-product">
          <h3 class="ml-9 mb-2 f-white">{{ type.name }}</h3>
          <hr>
          <div v-for="product in type.products" class="product d-flex my-4">
            <img :src="product.src">
            <div class="ml-6">
              <h4>{{ product.name }}</h4>
              <p>{{ product.description }}</p>
              </div>
              <span class="spacing">..............................................................................................................................................</span>
              <span class="ml-auto">{{ product.price }}</span>
              </div>

        </div>
      </v-container>
    </div>
  </div>
  <Contact />
</template>

<script>
export default {
  data() {
    return {
      all_products: [
        { id: 1, type: 1, name: "Tiramissú", description: "20 x 30cm", price: "35€", src: "/assets/tiramissu.jpg" },

        { id: 2, type: 1, name: "Cheesecake", description: "Diametro 20cm", price: "35€", src: "/assets/cheesecake.jpg" },

        { id: 3, type: 1, name: "Brownie", description: "22 x 28cm", price: "40€", src: "/assets/brownie.jpg" },

        { id: 4, type: 1, name: "Bolo de Tâmaras", description: "Diametro 20cm", price: "25€", src: "/assets/bolo-de-tamara.jpg" },

        { id: 5, type: 1, name: "Salted Caramel", description: "20 x 30cm", price: "40€", src: "/assets/salt-cramel.jpg" },

        { id: 6, type: 1, name: "Entremet Chocolat Crémeux", description: "Diametro 20cm", price: "60€", src: "/assets/chocolate-cremeux.jpg" },

        { id: 7, type: 1, name: "Charlote Pistachio Chocolate", description: "Diametro 20cm", price: "45€", src: "/assets/charlote-pistachio-chocolate.jpg" },

        { id: 7, type: 2, name: "Bola de Presunto", description: "2 bolas de 500g", price: "25€", src: "/assets/bola-de-presunto.jpg" },
      ],
      product_for_type: [
        { id: 1, name: "Desserts", products: [] },
        { id: 2, name: "Salty", products: [] },
      ]
    }
  },
  created() {
    for (let product_type of this.product_for_type) {
      product_type.products = this.all_products.filter(product => product.type == product_type.id)
    }
  },
}
</script>

<style scoped>

.section-menu {
  background-color: #121212;
}
.menu {
  background-color: #121212;
  position: relative;
  top: -100px;
}

.menu h2 {
  font-size: 40px;
  font-style: italic;
  font-weight: 100;
}

.menu h3 {
  font-weight: 100;
  font-size: 24px;
}

.menu h4, .menu span {
  font-weight: 100;
  font-size: 20px;
  color: #fff;
}
.menu p {
  font-size: 16px;
  color: #fff;
}


header {
  height: 400px;
  background-image: linear-gradient(to right, RGBA(0, 0, 0, 0.92), RGBA(0, 0, 0, 0.92)), url('/src/assets/icons/banner-site.jpg');
  background-position: top;
  background-size: contain;
  background-attachment: fixed;
}

.product .spacing {
  letter-spacing: 10px;
  overflow: hidden;
  text-align: center;
}

.product img {
  width: 100%;
  max-width: 100px;
  height: 100px;
  object-fit: cover;
}
</style>
