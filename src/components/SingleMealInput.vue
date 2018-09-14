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
              <containerCount :count=countVegetable containerType="vegetable" elementSize="large"/>
              <plusMinus signSymbol="-" v-on:update-count="countVegetable--"/>
              <plusMinus signSymbol="+" v-on:update-count="countVegetable++"/>
            </li>

            <li class="container-line">
              <span>Red Containers:</span>
              <containerCount :count=countProtein containerType="protein" elementSize="large"/>
              <plusMinus signSymbol="-" v-on:update-count="countProtein--"/>
              <plusMinus signSymbol="+" v-on:update-count="countProtein++"/>
            </li>

            <li class="container-line">
              <span>Yellow Containers:</span>
              <containerCount :count=countCarbohydrate containerType="carbohydrate" elementSize="large"/>
              <plusMinus signSymbol="-" v-on:update-count="countCarbohydrate--"/>
              <plusMinus signSymbol="+" v-on:update-count="countCarbohydrate++"/>
            </li>

            <li class="container-line">
              <span>Purple Containers:</span>
              <containerCount :count=countFruit containerType="fruit" elementSize="large"/>
              <plusMinus signSymbol="-" v-on:update-count="countFruit--"/>
              <plusMinus signSymbol="+" v-on:update-count="countFruit++"/>
            </li>

            <li class="container-line">
              <span>Blue Containers:</span>
              <containerCount :count=countHealthyFat containerType="healthyFat" elementSize="large"/>
              <plusMinus signSymbol="-" v-on:update-count="countHealthyFat--"/>
              <plusMinus signSymbol="+" v-on:update-count="countHealthyFat++"/>
            </li>

            <li class="container-line">
              <span>Orange Containers:</span>
              <containerCount :count=countSeedAndDressing containerType="seedAndDressing" elementSize="large"/>
              <plusMinus signSymbol="-" v-on:update-count="countSeedAndDressing--"/>
              <plusMinus signSymbol="+" v-on:update-count="countSeedAndDressing++"/>
            </li>

            <li class="container-line">
              <span>Teaspoons:</span>
              <containerCount :count=countTeaspoon containerType="teaspoon"/>
              <plusMinus signSymbol="-" v-on:update-count="countTeaspoon--"/>
              <plusMinus signSymbol="+" v-on:update-count="countTeaspoon++"/>
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
    }
  },
  data: function() {
    return {
      countVegetable: 0,
      countProtein: 0,
      countCarbohydrate: 0,
      countFruit: 0,
      countHealthyFat: 0,
      countSeedAndDressing: 0,
      countTeaspoon: 0
    };
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
