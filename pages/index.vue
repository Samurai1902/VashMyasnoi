<template>
  <div id="home" class="container">
    <FirstSection/>
    <Assortiment/>
    <ProductSlier/>
    <Request/>
  </div>
</template>

<script setup>
import Assortiment from '../components/home/assortiment.vue';
import FirstSection from '../components/home/firstSection.vue';
import ProductSlier from '../components/home/productSlier.vue';
import Request from '../components/home/request.vue';


</script>

<style>
#home{
  display: flex;
  flex-direction: column;
  z-index: 1;
}
</style>