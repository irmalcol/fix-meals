<template>
    <div class="single-meal-input">
        <h1>Meal Editor: {{ title }}</h1>
        <label>Title: </label>
        <input v-model="title" placeholder="New Meal">
        <label>Servings: </label>
        <input v-model="numberOfServings" placeholder=2>
        <br />

        <select v-model="containerCountGreen">
            <option>0</option>
            <option>1</option>
            <option>2</option>
            <option>3</option>
            <option>4</option>
        </select>
        <p>Green containers: {{ containerCountGreen }}</p>

        <select v-model="containerCountRed">
            <option>0</option>
            <option>1</option>
            <option>2</option>
            <option>3</option>
            <option>4</option>
        </select>
        <p>Red containers: {{ containerCountRed }}</p>

        <select v-model="containerCountYellow">
            <option>0</option>
            <option>1</option>
            <option>2</option>
            <option>3</option>
            <option>4</option>
        </select>
        <p>Yellow containers: {{ containerCountYellow }}</p>

        <div class="container-line">
          <span>Purple Containers:</span>
          <containerCount count=0 color="purple"/>
          <plusMinus signSymbol="-"/>
          <plusMinus signSymbol="+"/>
        </div>
    </div>
</template>

<script>
import plusMinus from "./interactive/plusMinus.vue";
import containerCount from "./containerCount.vue";

export default {
  name: "SingleMealInput",
  components: {
    plusMinus,
    containerCount
  },
  props: {
    title: {
      type: String,
      default: "New Meal"
    },
    containerCountGreen: {
      type: Number,
      default: 0
    },
    containerCountRed: {
      type: Number,
      default: 0
    },
    containerCountYellow: {
      type: Number,
      default: 0
    },
    containerCountPurple: {
      type: Number,
      default: 0
    }
  }
};
</script>

<style lang="scss" scoped>
$label-primary-color: #333;

.single-meal {
  color: $label-primary-color;
}

.container-line {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
