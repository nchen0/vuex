<template>
  <div id="app">
    <div id="nav">
      <h1>Vue App</h1>
      <product-list-one></product-list-one>
      <product-list-two v-bind:products="products"></product-list-two>
    </div>
    <router-view/>
  </div>
</template>
<script>
import ProductListOne from "./components/ProductListOne.vue";
import ProductListTwo from "./components/ProductListTwo.vue";

export default {
  name: "app",
  components: {
    "product-list-one": ProductListOne,
    "product-list-two": ProductListTwo
  },
  data() {
    return {};
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
