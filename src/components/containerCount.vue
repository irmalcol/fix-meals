<template>
    <div class="container-count">
        <span>99</span>
    </div>
</template>

<script>
export default {
  name: "containerCount",
  props: {
    count: {
      type: Number,
      default: 0
    },
    color: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="scss" scoped>
.container-count {
  display: inline-block;
  padding: 10px;
  text-align: center;
}

span {
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
