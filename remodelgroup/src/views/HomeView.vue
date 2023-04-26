<template>
  <div class="home">
    <div class="video">
      <video loop autoplay="autoplay" width="1920" :src='data.video' data-ready="true"></video>
    </div>
    <div class="list">
      <list-view origin="homelist" :listItems="data.homelist.items"></list-view>
    </div>
  </div>
</template>

<script setup>
import { ListView } from "@/components";
import {homeData} from '@/lib/staticData.js'
import { reactive } from 'vue'
const data = reactive({
    homelist: homeData,
    video: "https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ElephantsDream.mp4"
})
</script>

<style scoped>
.video {
  height: 60vh;
  width: 100vw;
  object-fit: fill;
}
.list {
 margin-left: 12%;
}
</style>



