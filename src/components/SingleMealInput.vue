<template>
    <div class="single-meal-input">
        <h1>Meal Editor: {{ title }}</h1>
        <label>Title: </label>
        <input v-model="title" placeholder="New Meal">
        <label>Servings: </label>
        <input v-model="numberOfServings" placeholder="Enter a whole number">
        <br />

        <div class=centering>
          <ul class="container-listing">
            <li class="container-line">
              <span>Green Containers:</span>
              <containerCount count=0 color="green"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Red Containers:</span>
              <containerCount count=0 color="red"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Yellow Containers:</span>
              <containerCount count=0 color="yellow"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Purple Containers:</span>
              <containerCount count=0 color="purple"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Blue Containers:</span>
              <containerCount count=0 color="blue"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Orange Containers:</span>
              <containerCount count=0 color="orange"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Teaspoons:</span>
              <containerCount count=0 color="grey"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>
          </ul>
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

.container-listing {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  align-items: flex-end;
  width: 350px;
  margin-left: auto;
  margin-right: auto;
  padding: 0;
}

.container-line {
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
</style>
