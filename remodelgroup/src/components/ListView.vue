<template>
    <div class="listC">
        <div class="list" v-for="(item, index) in props.listItems" :key="index">
            <template v-if="props.origin == 'products'">
                <product-tile :productItem="item" :index="index"></product-tile>
            </template>
        </div>
    </div>
</template>
<script setup>
import {ProductTile} from "@/components";
import { defineProps } from 'vue';

const props = defineProps(['listItems', 'origin'])
</script>
<style scoped>
.listC{ 
    display: flex;
    overflow-x: scroll;
}

.listC::-webkit-scrollbar {
  width: 0;
}

.list {
    margin-right: 20px;
}
</style>