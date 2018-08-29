<template>
    <div class="single-meal">
        <select v-model="selectedRed">
            <option>0</option>
            <option>1</option>
            <option>2</option>
            <option>3</option>
            <option>4</option>
        </select>
        <p>Green containers: {{ selectedRed }}</p>
    </div>
</template>

<script>
export default {
  name: "SingleMeal"
};
</script>

<style lang="scss" scoped>
.single-meal {
  color: red;
}
</style>
