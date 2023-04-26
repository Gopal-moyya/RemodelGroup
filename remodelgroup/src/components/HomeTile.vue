<template>
  <div class="listitem">
    <div class="logo">
      <img alt="logo"   :src="props.homelistItem.logo" width="95" height="71"/>
    </div>
    <div class="text">
      <h3>{{props.homelistItem.title}}</h3>
      <p>{{props.homelistItem.description}}</p>
    </div>
  </div>
</template>
<script setup>
import { defineProps } from "vue";
const props = defineProps(["homelistItem", "index"]);
</script>
<style scoped>
.listitem {
  margin-right:-20px;
  width:411px;
  height:300px;
  background: #ffffff;
  box-shadow: 1px 10px 15px 8px lightgrey;
  text-align: center;
}
.logo{
  height: 100px;
  padding-top: 33px;
  color: #000000;
  alignment: center;
}
.text {
  text-align: center;
  padding:30px;
  color: #000000;
}
</style>