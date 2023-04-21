<template>
  <div class="listitem">
  <img alt="logo" :src="data.image" width="95px" height="71px"/>
  <h2>{{data.title}}</h2>
   <p>{{data.description}}</p>
  </div>
</template>

<script>
export default {
  name: 'ListItem',
  props: {
    data : Object
  }
}
</script>

<style scoped>
.listitem {
    margin-left: 138px;
    margin-top: -60px;
    width:411px;
    height:300px;
    background: #ffffff;
    align-content:center;
    align-items: center;
}
img{
    color: #000000;
}
h2 {
   color: #cb0000;

}
p {
    color: #000000;
}
</style>