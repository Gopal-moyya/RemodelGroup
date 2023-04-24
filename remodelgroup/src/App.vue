<template>
    <h1>Remodelgroup</h1>
    <nav>
    <router-link to="/">Home</router-link>
    <router-link to="/projects">Projects</router-link> 
    <router-link to="/products">Products</router-link>
    <router-link to="/contact">Contact</router-link>
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav a{
  font-weight: bold;
  color: #000000;
  padding-right: 50px;
  text-align: right;
  font-size: 25px;
}

nav {
  padding: 30px;
}

nav a.router-link-exact-active {
  color: #42b983;
}
h1 {
  font-family:'Arial Narrow Bold';
  text-align: left;
  vertical-align: top;
}
</style>
