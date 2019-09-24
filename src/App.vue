<template>
  <div id="app">
    <Header/>
    <Cocktail v-bind:cocktails="cocktails.drinks" />
  </div>
</template>

<script>
import Cocktail from "./components/Cocktail";
import axios from "axios";
import Header from "./components/layout/Header";

export default {
  name: "app",
  components: {
    Cocktail,
    Header
  },
  data() {
    return {
      cocktails: []
    };
  },
  created() {
    axios.get('https://www.thecocktaildb.com/api/json/v1/1/random.php')
    .then(res => this.cocktails = res.data)
    .catch(err => console.log(err));
  }
};
</script>

<style>
* {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  justify-content: center;
}

#app {
  width: 50%;
  margin: 0 auto;
}

body {
  background-color: black;
}
</style>
