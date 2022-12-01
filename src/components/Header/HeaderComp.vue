<template>
  <header>
    <a href="#" class="logo">LOGO</a>
    <div class="buttons">
      <button><img src="../../assets/icons/person.svg" alt=""></button>
      <button><img src="../../assets/icons/favorite.svg" alt=""></button>
      <button><img src="../../assets/icons/bag.svg" alt=""></button>
      <button class="menu-icon" @click="openMenu"><img src="../../assets/icons/menu.png" alt=""></button>
    </div>
  </header>
  <div class="menu" v-if="isOpenMenu">
    <button class="close-menu" @click="closeMenu">X</button>
    <a href="#">постельное белье</a>
    <a href="#">одежда для дома</a>
    <a href="#">Одежда для улицы</a>
    <a href="#">ВЫход</a>
  </div>
</template>

<script>
export default {
  name: "HeaderComp",
  data() {
    return {
      isOpenMenu: false
    }
  },
  methods: {
    openMenu() {
      this.isOpenMenu = !this.isOpenMenu;
    },
    closeMenu() {
      this.isOpenMenu = !this.isOpenMenu;
    }
  }
}
</script>
<style src="./header.css"></style>
