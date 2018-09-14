<template>
    <div class="single-meal-view">
        <h1>{{ title }}</h1>
        <span>Serves {{ numberOfServings }}</span>
        <div data-icon="ei-pencil" data-size="m"></div>
        <ul class="container-heading">
            <li class="container-line">
                <containerCount :count=countVegetable containerType="vegetable" elementSize="small"/>
            </li>

            <li class="container-line">
                <containerCount :count=countProtein containerType="protein" elementSize="small"/>
            </li>

            <li class="container-line">
                <containerCount :count=countCarbohydrate containerType="carbohydrate" elementSize="small"/>
            </li>

            <li class="container-line">
                <containerCount :count=countFruit containerType="fruit" elementSize="small"/>
            </li>

            <li class="container-line">
                <containerCount :count=countHealthyFat containerType="healthyFat" elementSize="small"/>
            </li>

            <li class="container-line">
                <containerCount :count=countSeedAndDressing containerType="seedAndDressing" elementSize="small"/>
            </li>

            <li class="container-line">
                <containerCount :count=countTeaspoon containerType="teaspoon" elementSize="small"/>
            </li>
        </ul>
    </div>
</template>

<script>
import containerCount from "./containerCount.vue";

export default {
  name: "SingleMealView",
  components: {
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
      countTeaspoon: 0,
      numberOfServings: 0
    };
  }
};
</script>

<style lang="scss" scoped>
$label-primary-color: #333;

.single-meal {
  color: $label-primary-color;
}

.container-heading {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  //   width: 350px;
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
