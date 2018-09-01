<template>
    <div class="plus-minus">
        <a href="#">{{signSymbol}}</a>
    </div>
</template>

<script>
export default {
  name: "plusMinus",
  props: {
    signSymbol: {
      type: String,
      default: "+"
    }
  }
};
</script>

<style lang="scss" scoped>
.plus-minus {
  display: inline-block;
  padding: 10px;
  text-align: center;
}

a {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 2px black solid;
  border-radius: 5px;
  height: 40px;
  width: 40px;
  background-color: #eee;
}
</style>
