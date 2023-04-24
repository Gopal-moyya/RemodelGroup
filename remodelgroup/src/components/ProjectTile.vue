<template>
  <div class="outer">
    <div class="projectImage">
      <img :src="props.projectItem.logo" height="250" width="380" />
    </div>
    <div class="projectInfo">
      <div class="projectTitle">{{ props.projectItem.title }}</div>
      <div class="projectDesc">{{ props.projectItem.desc }}</div>
      <a class="projectLink" href="props.productItem.link">Project link</a>
    </div>
  </div>
  <div class="endLine"><hr></div>
</template>
<script setup>
import { defineProps } from "vue";

const props = defineProps(["projectItem", "index"]);
</script>
<style scoped>
.outer {
  cursor: pointer;
  display: flex;
   align-items: start;
}
/* .projectInfo{
   box-sizing: border-box;
  margin: auto;
 border: 3px solid #73AD21;
  width: 400px;
 float: left;
  text-align: left;
  align-items: flex-start;
} */
.projectTitle {
  overflow: hidden;
  max-height: 48px;
  font-size: 18px;
  font-weight: 700;
  line-height: 24px;
  margin: 22px 0 0;
  color: #0886d7;
}
.projectTitle:hover {
  color: #5996d7;
}
.projectDesc {
  overflow: hidden;
  max-height: 100px;
  line-height: 20px;
  padding-top: 14px;
  font-weight: 700;
  font-size: 13px;
  font-family: sans-serif;
  font-style: bold;
  margin-bottom: 20px;
}
.projectLink {
  color: #5996d7;
}
.projectInfo {
  font-size: 20px;
  padding-left: 70px;

  
}
.endLine{
  margin-top: 30px;
}
</style>