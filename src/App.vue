<template>
  <header-comp/>
  <product-details/>
  <all-styles/>
  <footer-comp/>
</template>
<script>
import HeaderComp from "@/components/Header/HeaderComp";
import ProductDetails from "@/components/ProductDetails/ProductDetails";
import AllStyles from "@/components/AllStyles/AllStyles";
import FooterComp from "@/components/FooterComp/FooterComp";

export default {
  name: 'App',
  components: {
    FooterComp,
    AllStyles,
    ProductDetails,
    HeaderComp
  }
}
</script>
<style src="./assets/main.css"></style>
