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
        { id: 1, type: 1, name: "Tiramissú", description: "20 x 30cm", price: "35€", src: "src/assets/icons/tiramissu.jpg" },

        { id: 2, type: 1, name: "Cheesecake", description: "Diametro 20cm", price: "35€", src: "src/assets/icons/cheesecake.jpg" },

        { id: 3, type: 1, name: "Brownie", description: "22 x 22cm", price: "40€", src: "src/assets/icons/brownie.jpg" },

        { id: 4, type: 1, name: "Bolo de Tâmaras", description: "Diametro 20cm", price: "25€", src: "src/assets/icons/bolo-de-tamara.jpg" },

        { id: 5, type: 1, name: "Salt Caramel", description: "20 x 30cm", price: "40€", src: "src/assets/icons/salt-cramel.jpg" },

        { id: 6, type: 1, name: "Entremet Chocolat Cremely", description: "Diametro 20cm", price: "60€", src: "src/assets/icons/chocolate-cremeux.jpg" },

        { id: 7, type: 1, name: "Charlote Pistachio Chocolate", description: "Diametro 20cm", price: "45€", src: "src/assets/icons/charlote-pistachio-chocolate.jpg" },
      ],
      product_for_type: [
        { id: 1, name: "Desserts", products: [] },
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
[{id: 1, name: Tiramissú, description:  20 x 30cm / 35€},

{id: 2, name: Cheesecake, description: Diametro 20cm / 35€},

{id: 3, name: Brownie, description: 22 x 22cm / 40€},

{id: 4, name: Bolo de Tâmaras, description: Diametro 20cm / 25€},

{id: 5, name: Salt Caramel, description: 20 x 30cm / 40€},

{id: 6, name: Entremet Chocolat Cremely, description:Diametro 20cm / 60€},

{id: 7, name: Charlote Pistachio Chocolate, description: Diametro 20cm / 45€},]
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
  background-image: linear-gradient(to right, RGBA(0, 0, 0, .7), RGBA(0, 0, 0, .7)), url('/src/assets/icons/header.png');
  background-position: center;
  background-size: cover;
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
