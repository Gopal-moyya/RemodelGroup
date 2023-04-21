<template>
    <div class="outer">
        <div class="productImage">
            <img :src="props.productItem.logo" height="250" width="175">
        </div>
        <div class="productInfo">
            <div class="productTitle">{{props.productItem.title}}</div>
            <div class="productDesc">{{props.productItem.desc}}</div>
            <a class="productLink" href="props.productItem.link">Product link</a>
        </div>
    </div>
</template>
<script setup>
import { defineProps} from 'vue'

const props = defineProps(['productItem', 'index'])

</script>
<style scoped>
.outer {
    border: 1px solid lightgrey;
    width: 250px;
    padding: 20px;
    cursor: pointer;
    word-break:break-word;
}
.outer:hover {
    border-color: #5996d7;
}
.productImage {
    margin-left: 40px;
}
.productInfo {
    text-align: left;
}
.productTitle {
    font-size: 18px;
    font-weight: 700;
    line-height: 24px;
    margin: 22px 0 0;
    color: #0886d7;
}
.productTitle:hover {
    color: #5996d7
}
.productDesc {
    line-height: 20px;
    padding-top: 14px;
    font-weight: 700;
    font-size: 13px;
    font-family: sans-serif;
    font-style: bold;
    margin-bottom: 20px;
}
.productLink {
    color: #5996d7
}
</style>