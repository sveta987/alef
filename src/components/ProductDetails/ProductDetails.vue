<template>
  <div class="product-description">
    <div class="image-section">
      <img :src="`/images/${currentImage}.png`" class="main-image">
      <div class="image-select">
        <div v-for="(image, index) in images" @click="changeMainImage(index)" >
          <div v-show=" images[index] !==currentImage"  class="overlay"></div>
          <img :src="`/images/${image}.png`" >
        </div>
      </div>

    </div>
    <div class="content">
      <div class="description-section">
        <h3 class="heading">Пижама для девочек</h3>
        <p class="code">Арт. 02765/46</p>
        <div class="reviews">
          <p class="review">Отзывы</p>
          <div class="stars">
            <div v-for="(rate, index) in ratings" :key="index">
              <button @click="rate_value=index">
                <img v-if="index > rate_value" src="../../assets/icons/star.png">
                <img v-else src="../../assets/icons/star-full.png">
              </button>
            </div>
          </div>
          <p class="review">14 отзывов </p>
          <button class="arrow">
            <img  src="../../assets/icons/arrow.png">
          </button>
        </div>
      </div>
      <div class="price-section">
        <h2 class="price">800 ₽</h2>
        <h4 class="old-price">1 500 ₽</h4>
      </div>
      <div class="discount-section">
        <div class="discount">
          <p>скидка -36%</p>
        </div>
        <div class="discount">
          <p>акция -20%</p>
        </div>
      </div>
      <div class="size-section">
        <select name="sizes" id="sizes" v-model="size">
          <option value=""> Выбрать размер </option>
          <option value="s"> S </option>
          <option value="m"> M </option>
          <option value="l"> L </option>
        </select>
        <a href="#">Определить размер</a>
      </div>
      <div class="add-to-card-section">
        <div class="buttons-part">
          <div class="buttons">
            <button class="inc-dec" @click="count--" :disabled="count<=1">-</button>
            <span class="inc-dec">{{ count }}</span>
            <button class="inc-dec" @click="count++">+</button>
          </div>
          <button class="add-to-card">Добавить в корзину</button>
          <button class="add-to-favorite" @mouseenter="isHoverFavorite = !isHoverFavorite" @mouseleave="isHoverFavorite = !isHoverFavorite">
            <img v-if="isHoverFavorite" src="../../assets/icons/favorite.svg" alt="">
            <img v-else src="../../assets/icons/white-heart.png" alt="">
          </button>
        </div>
        <a href="#">Купить в 1 клик</a>
      </div>
      <hr class="straight-line"/>
      <div class="fast-links">
        <div class="link">
          <img src="../../assets/icons/desc.png">
          <a href="#">
            Описание товара
          </a>
        </div>
        <div class="link">
          <img src="../../assets/icons/clock.png">
          <a href="#">
           Доставка и возврат
          </a>
        </div>
        <div class="link">
          <img src="../../assets/icons/wallet.png">
          <a href="#">
           Способы оплат
          </a>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: "ProductDetails",
  data(){
    return{
      images:['s-1', 's-2','s-3','s-4','s-5'],
      currentImage: null,
      ratings: [1, 2, 3, 4, 5],
      rate_value: null,
      size:'',
      count:1,
      isHoverFavorite: false
    }
  },
  methods:{
    changeMainImage(index){
      this.currentImage = this.images[index];
    },
  },
  mounted() {
    this.currentImage = this.images[0];
  }
}
</script>

<style src="./productDetails.css"></style>
