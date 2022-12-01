<template>
  <div class="all-styles">
    <a href="#" class="all-styles-link">Посмотреть все стили</a>
  </div>
  <div class="image-section">
    <div class="left-side">
      <div class="image-container">
        <img src="../../assets/images/all-1.png" alt="">
        <div class="overlay">
          <div class="content">
            <button class="full-screen"><img src="../../assets/icons/full-screen.svg" alt=""></button>
            <button><img src="../../assets/icons/white-bag.png" alt=""></button>
            <p>Узнай, что на мне</p>
            <div class="favorite">
              <button><img src="../../assets/icons/favorite-full.svg" alt=""></button>
              <p>{{ favoriteCount }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="right-side">
      <div class="row">
        <div class="image-container">
          <img src="../../assets/images/all-2.png" alt="">
          <div class="overlay">
            <div class="content">
              <button class="full-screen"><img src="../../assets/icons/full-screen.svg" alt=""></button>
              <button><img src="../../assets/icons/white-bag.png" alt=""></button>
              <p>Узнай, что на мне</p>
              <div class="favorite">
                <button><img src="../../assets/icons/favorite-full.svg" alt=""></button>
                <p>{{ favoriteCount }}</p>
              </div>
            </div>
          </div>
        </div>
        <div class="image-container">
          <img src="../../assets/images/all-3.png" alt="">
          <div class="overlay">
            <div class="content">
              <button class="full-screen"><img src="../../assets/icons/full-screen.svg" alt=""></button>
              <button><img src="../../assets/icons/white-bag.png" alt=""></button>
              <p>Узнай, что на мне</p>
              <div class="favorite">
                <button><img src="../../assets/icons/favorite-full.svg" alt=""></button>
                <p>{{ favoriteCount }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="image-container">
          <img src="../../assets/images/all-4.png" alt="">
          <div class="overlay">
            <div class="content">
              <button class="full-screen"><img src="../../assets/icons/full-screen.svg" alt=""></button>
              <button><img src="../../assets/icons/white-bag.png" alt=""></button>
              <p>Узнай, что на мне</p>
              <div class="favorite">
                <button><img src="../../assets/icons/favorite-full.svg" alt=""></button>
                <p>{{ favoriteCount }}</p>
              </div>
            </div>
          </div>
        </div>
        <div class="image-container">
          <img src="../../assets/images/all-5.png" alt="">
          <div class="overlay">
            <div class="content">
              <button class="full-screen"><img src="../../assets/icons/full-screen.svg" alt=""></button>
              <button><img src="../../assets/icons/white-bag.png" alt=""></button>
              <p>Узнай, что на мне</p>
              <div class="favorite">
                <button><img src="../../assets/icons/favorite-full.svg" alt=""></button>
                <p>{{ favoriteCount }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: "AllStyles",
  data(){
    return{
      favoriteCount:null,
    }
  },
  mounted() {
    this.favoriteCount = 200;
  }
}
</script>
<style src="./allStyles.css"></style>
<style src="./allStylesMedia.css"></style>
