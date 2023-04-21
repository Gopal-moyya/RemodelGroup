<template>
  <div class="home"> 
    <video loop width="1920" height="869" autoplay="autoplay" :src='video' data-ready="true"></video>
    <ul>
    <ListItem
      v-for="item in data"
      :data = item
      :key="item.id"
    />
    </ul>
  </div>
</template>

<script>
// @ is an alias to /src
import ListItem from '@/components/ListItem.vue'
import {homeData} from '@/lib/staticData.js'

export default {
  name: 'HomeView',
  data(){
    return {
      data : homeData.items,
      video: "http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4"
    }
  },
  components: {
    ListItem
  }
}
</script>

<style scoped>
ul{
  display: flex;
}
</style>



