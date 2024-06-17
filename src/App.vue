<template>
  <div>
    <!--    <div v-if="isVisible" class="red">red</div>
        <div v-if="isVisible === true" class="blue">blue</div>
        <div v-else class="white">white</div>-->

    <!--    <div v-if="count > 1" class="red"></div>
        <div v-else class="blue"></div>-->

    <div v-show="isVisible" class="red"></div>
    <div v-show="!isVisible" class="blue"></div>
    <!--    <button @click="count++">Up</button>
        <button @click="count&#45;&#45;">Down</button>-->

    <button @click="isVisible = true">isVisible</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: false
      , count: 0
    }
  }
}
</script>

<style scoped>
.red {
  width: 100px;
  height: 100px;
  background-color: red;
}

.blue {
  width: 100px;
  height: 100px;
  background-color: blue;
}

.white {
  width: 100px;
  height: 100px;
  background-color: white;
}
</style>
