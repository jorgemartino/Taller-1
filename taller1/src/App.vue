
<template>
    <div id="app">
      <div class="jumbotron jumbotron-fluid bg-primary">
      <img src="logo.png" class="float-left"> 
      <HelloWorld msg=" -Formulario de Préstamo- " />
    </div>
    <formulario />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import formulario from "./components/formulario.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    formulario
  }
};
</script>
s
<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
