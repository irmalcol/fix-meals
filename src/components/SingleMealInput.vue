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
              <containerCount :count=this.containerCountGreen containerType="vegetable"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Red Containers:</span>
              <containerCount :count=this.containerCountRed containerType="protein"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Yellow Containers:</span>
              <containerCount :count=this.containerCountYellow containerType="carbohydrate"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Purple Containers:</span>
              <containerCount :count=this.containerCountPurple containerType="fruit"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Blue Containers:</span>
              <containerCount :count=this.containerCountBlue containerType="healthyFat"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Orange Containers:</span>
              <containerCount :count=this.containerCountOrange containerType="seedAndDressing"/>
              <plusMinus signSymbol="-"/>
              <plusMinus signSymbol="+"/>
            </li>

            <li class="container-line">
              <span>Teaspoons:</span>
              <containerCount :count=this.containerCountTeaspoon containerType="teaspoon"/>
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
      default: 11
    },
    containerCountRed: {
      type: Number,
      default: 12
    },
    containerCountYellow: {
      type: Number,
      default: 13
    },
    containerCountPurple: {
      type: Number,
      default: 14
    },
    containerCountBlue: {
      type: Number,
      default: 15
    },
    containerCountOrange: {
      type: Number,
      default: 16
    },
    containerCountTeaspoon: {
      type: Number,
      default: 17
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
