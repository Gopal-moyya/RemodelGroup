<template>
    <div class="listC">
        <div class="list" v-for="(item, index) in props.listItems" :key="index">
            <template v-if="props.origin == 'projects'">
                <ProjectTile :projectItem="item" :index="index"></ProjectTile>
            </template>
        </div>
    </div>
</template>
<script setup>
import {ProjectTile} from "@/components";
import { defineProps } from 'vue';

const props = defineProps(['listItems', 'origin'])
</script>
<style scoped>
.listC{ 
    display: flex;
    flex-direction: column;
    overflow-x: scroll;
} 
.listC::-webkit-scrollbar {
  width: 0;
}

 .list {
    margin-bottom: 30px;
}
</style>