<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <SingleMealInput title="Test Meal Name - Input"/>
    <SingleMealView title="Test Meal Name - View"/>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import SingleMealInput from "./components/SingleMealInput.vue";
import SingleMealView from "./components/SingleMealView.vue";

export default {
  name: "app",
  components: {
    // HelloWorld,
    SingleMealInput,
    SingleMealView
  }
};
</script>

<style lang="scss">
@import "css/normalize.css";

$label-primary-color: #333;

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  font-size: 18px; //Refactor this out
}

input {
  font-size: 18px; //Refactor this out
}

a {
  text-decoration: none;
  color: $label-primary-color;
}
</style>
