<template>
  <footer>
    <div class="box">
      <h4 class="heading">покупателям</h4>
      <a class="link" href="#">Каталог</a>
      <a class="link" href="#">Акции</a>
      <a class="link" href="#">Бренды</a>
    </div>
    <div class="box">
      <h4 class="heading">о нас</h4>
      <a class="link" href="#">О компании</a>
      <a class="link" href="#">Новости</a>
      <a class="link" href="#">Команда</a>
    </div>
    <div class="box">
      <h4 class="heading">Узнайте первыми о новинках и акциях</h4>
      <div class="input-area">
        <input type="email" v-model="email" id="email" placeholder="Адрес электронной почты">
        <label @click="email=''" for="email"><img src="../../assets/icons/x.png" alt=""></label>
      </div>
      <p v-if="incorrectEmail" class="incorrect-email">* Ваш адрес электронной почты неверен, пожалуйста, исправьте
        это</p>
      <button @click="checkEmail">Подписаться</button>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComp",
  data() {
    return {
      email: null,
      incorrectEmail: false,
    }
  },
  methods: {
    checkEmail() {
      if (!this.email.includes('@')) this.incorrectEmail = true;
      else {
        this.incorrectEmail = false;
        this.email = '';
      }
    }
  }
}
</script>
<style src="./footerComp.css"></style>
<style src="./FooterCompMedia.css"></style>
