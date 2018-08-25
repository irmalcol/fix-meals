<template>
    <div class="single-meal">
        <p>{{ msg }}</p>
    </div>
</template>

<script>
export default {
  name: "SingleMeal",
  props: {
      msg: String
  }
};
</script>

<style lang="scss" scoped>
    .single-meal {
        color: red;
    }
</style>
