<template>
  <div id="app">
    <Cocktail v-bind:cocktails="cocktails.drinks" />
  </div>
</template>

<script>
import Cocktail from "./components/Cocktail";
import axios from "axios";

export default {
  name: "app",
  components: {
    Cocktail
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
  color: white;
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
