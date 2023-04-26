<template>
  <div class="outer">
    <div class="banner">
      <img :src="data.projectsData.bannerImage" width="1300" height="450" />
    </div>
    <div class="projectInfo">
      <div class="bannerInfo">{{ data.projectsData.tagline }}</div>
      <div class="projectsTitle">{{ data.projectsData.title }}</div>
      <div class="desc1">{{ data.projectsData.desc1 }}</div>
        </div>
       <div class="listItems">
      <ProjectList
        origin="projects"
        :listItems="data.projectsData.projects"
      ></ProjectList>
  
    </div>
  </div>
</template>
<script setup>
import { ProjectList } from "@/components";
import { projects } from "@/lib/staticData";
import { reactive } from "vue";
console.log(projects);
const data = reactive({
  projectsData: projects,
});
</script>
<style scoped>
.projectInfo {
  box-sizing: border-box;
  margin: auto;
  padding: 40px;
  position: relative;
    /* border: 3px solid #73AD21; */
  width: 100%;
  max-width: 1024px;
  text-align: left;
}
.listItems {
  box-sizing: border-box;
  margin: auto;
  position: relative;
  padding-left:155px;
    /* border: 3px solid #73AD21; */
  width: 1280px;
  /* max-width: 1024px; */
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
.projectsTitle {
  color: #00c858;
  font-size: 30px;
  font-style: bold;
  line-height: 42px;
  margin: 22px 0 44px;
}
.desc1 {
  font-weight: 600;
  line-height: 22px;
  margin: 22px 0 50px 0;
}
</style>