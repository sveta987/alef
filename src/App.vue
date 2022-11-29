<template>
  <header-comp />
  <product-details />
</template>

<script>


import HeaderComp from "@/components/Header/HeaderComp";
import ProductDetails from "@/components/ProductDetails/ProductDetails";
export default {
  name: 'App',
  components: {
    ProductDetails,
    HeaderComp
  }
}
</script>
<style src="./assets/main.css"></style>
