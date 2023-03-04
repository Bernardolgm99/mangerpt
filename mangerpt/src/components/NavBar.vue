<template>
  <div>
    <div class="d-md-none menu-mobile d-flex flex-column align-center" :class="{menuMobileOpen: !menu_mobile_open}">
      <div class="menu-mobile-text pointer py-15 w-100 mt-16" @click="goHome">home</div>
      <hr color="#999" class="w-75">
      <div class="menu-mobile-text pointer py-15 w-100" @click="goMenu">menu</div>
      <hr color="#999" class="w-75">
      <div class="menu-mobile-text pointer py-15 w-100">contact</div>
    </div>
  </div>
  <nav class="conteiner">
    <v-container class="pa-0">
      <v-row class="ma-0">
        <v-col class="d-md-none"></v-col>
        <v-col class="d-flex justify-center">
          <div>
            <img class='pointer' style="width:39px" src="/src/assets/icons/hat1.png" @click="goHome">
          </div>
        </v-col>
        <v-col class="d-none d-md-block pa-0">
          <div class="d-flex justify-space-between h-100">
            <div class="navegationBtn pointer d-flex align-center px-10" @click="goHome"><span>home</span></div>
            <div class="navegationBtn pointer d-flex align-center px-10" @click="goMenu"><span>menu</span></div>
            <div class="navegationBtn pointer d-flex align-center px-10"><span>contact</span></div>
          </div>
        </v-col>
        <v-col class="d-none d-md-block"></v-col>
        <v-col class="d-md-none d-flex justify-end">
          <div class="menu-btn pointer me-3" @click="openMenu">
            <div class="menu-burger" :class='{ open: menu_mobile_open }'></div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      menu_mobile_open: false,
    }
  },
  methods: {
    openMenu() {
      if (this.menu_mobile_open) {
        this.menu_mobile_open = false;
      }
      else {
        this.menu_mobile_open = true;
      }
    },
    goMenu() {
      this.$router.push({name:'menu'});
    },
    goHome() {
      this.$router.push({name:'home'});
    },
  },
}
</script>

<style scoped>
nav {
  position: fixed;
  height: 64px;
  width: 100vw;
  background-color: #e3e3e3e3;
  z-index: 1;
}
.menu-btn {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 40px;
  width: 40px;
  border-radius: 100%;
}

.menu-btn:active {
  background-color: rgba(0, 0, 0, 0.2);
}

.menu-burger {
  width: 20px;
  height: 5px;
  background-color: rgb(20, 20, 20);
  border-radius: 5px;
  transition: all .3s ease-in-out;
  transform: translateX(-2.5px);

}

.menu-burger::before,
.menu-burger::after {
  content: '';
  position: absolute;
  width: 25px;
  height: 5px;
  background-color: rgb(20, 20, 20);
  border-radius: 5px;
  transition: all .3s ease-in-out;
}

.menu-burger::before {
  transform: translateY(-10px);
}

.menu-burger::after {
  transform: translateY(10px);
}

.open {
  transform: translateX(-25px);
  background: transparent;
}

.open::before {
  transform: rotate(-45deg) translate(16px,16px);
}
.open::after {
  transform: rotate(45deg) translate(16px,-16px);
}

.menu-mobile {
  position: fixed;
  z-index: 1;
  width: 100vw;
  height: 100vh;
  background-color: #e3e3e3;
  transition: all .4s ease-in-out;
}

.menuMobileOpen {
  transform: translateY(-100vh);
}

.menu-mobile-text {
  font-size:25px;
  text-align: center;;
}

.menu-mobile-text:active {
  transition: all .2s ease-in-out;
  background-color: rgba(0, 0, 0, 0.2);
}

.navegationBtn {
  font-size: 18px;
  padding: 10px 80px;
}

.navegationBtn:hover {
  background-color: #8c311f99;
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

