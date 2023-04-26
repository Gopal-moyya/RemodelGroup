<template>
  <div class="outer">
    <div class="banner">
      <img :src="data.productsData.bannerImage" width="1280" height="480" >
    </div>
    <div class="productInfo">
      <div class="bannerInfo">{{data.productsData.tagline}}</div>
      <div class="productsTitle">{{data.productsData.title}}</div>
      <div class="desc1">{{data.productsData.desc1}}</div>
      <div class="desc2">{{data.productsData.desc2}}</div>
      <list-view origin="products" :listItems="data.productsData.products"></list-view>
    </div>
  </div>
</template>
<script setup>
import { ListView } from "@/components";
import { products } from "@/lib/staticData";
import { reactive } from 'vue'
console.log(products)
const data = reactive({
  productsData: products,
})
</script>
<style scoped>
.banner {
  max-width: 1280;
  width: 100%;
}
.productInfo {
  box-sizing: border-box;
  margin: auto;
  padding: 40px;
  position: relative;
  width: 100%;
  max-width: 1024px;
  text-align: left;
}
.bannerInfo {
  color: #999;
  font-weight: 600;
  line-height: 22px;
  font-family: sans-serif;
  margin-left: 0;
}
.bannerInfo:hover {
  color: #4db5f8;
  cursor: pointer;
}
.productsTitle {
  color: #00c858;
  font-size: 30px;
  font-style: bold;
  line-height: 42px;
  margin: 22px 0 44px;
}
.desc1 {
  font-weight: 700;
  line-height: 26px;
  margin: 22px 0 22px 0;
}
.desc2 {
  margin: 22px 0 22px 0;
}
</style>