<template>
    <div class="container-count">
        <span :class=this.color>{{count}}</span>
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

.green {
  background-color: #18d315;
}
.red {
  background-color: #ff4242;
}
.yellow {
  background-color: #ffe44f;
}
.purple {
  background-color: #895ffc;
}
.blue {
  background-color: #4e4efc;
}
.orange {
  background-color: #fcad2d;
}
.grey {
  background-color: #e2e2e2;
}
</style>
