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
    video: "http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4"
})
</script>

<style scoped>
.video {
  width: 1920px;
  height: 869px;
}
.list {
 margin-left: 138px;
}
</style>



