<template>
    <div class="container-count">
        <span :class=this.containerType>{{count}}</span>
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
    containerType: {
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

.vegetable {
  background-color: #18d315;
}
.protein {
  background-color: #ff4242;
}
.carbohydrate {
  background-color: #ffe44f;
}
.fruit {
  background-color: #895ffc;
}
.healthyFat {
  background-color: #4e4efc;
}
.seedAndDressing {
  background-color: #fcad2d;
}
.teaspoon {
  background-color: #e2e2e2;
}
</style>
