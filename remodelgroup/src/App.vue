<template>
  <div id="app">
    <div class="bg">
      <div class="header">
        <div class = "logo">
        <img src="./assets/header.png" width="150" height="150" />
        </div>
        <nav class="menu">
          <router-link to="/">Home</router-link>
          <router-link to="/projects">Projects</router-link>
          <router-link to="/products">Products</router-link>
          <router-link to="/contact">Contact</router-link>
        </nav>
      </div>
      <router-view/>
    </div>
  </div>
</template>

<style>
#app {
  font-family: "Poppins","PoppinsMedium", serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: inherit;
  width: inherit;
}

@font-face {
  font-family: "Poppins";
  font-weight: 400;
  font-style: normal;
  font-display: auto;
  unicode-range: U+000-5FF;
  src: local("Poppins"), url("./assets/fonts/Poppins-Light.ttf") format("truetype");
}

@font-face {
  font-family: "PoppinsMedium";
  font-weight: 400;
  font-style: normal;
  font-display: auto;
  unicode-range: U+000-5FF;
  src: local("Poppins"), url("./assets/fonts/Poppins-Medium.ttf") format("truetype");
}

.bg {
  height: 100%;
  background-image: url('./assets/background.jpg') !important;
  width: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.header{
  display: flex;
  flex-direction: row;
}

.logo {
  height: 100px;
  flex-grow: 3;
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
}

.menu {
  height: 100px;
  width: auto;
  background-position: right;
  flex-grow: 1;
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;
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
  font-family:'PoppinsMedium';
  text-align: left;
  vertical-align: top;
}
</style>
