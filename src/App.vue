<template>
  <div id="app">
    <Nav /> 
    <Main />
    <Foot />

    <router-view></router-view>
  </div>
</template>

<script>
/* eslint-disable */
import Nav from "@/components/Nav.vue"; 
import Main from "@/components/Main.vue"; 
import Foot from "@/components/Foot.vue"; 

export default {
  name: "App",
  components: {
    Foot,
    Main,
    Nav
  }
  //console.log("hello")
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>
