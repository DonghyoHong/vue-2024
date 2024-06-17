<template>
  <div>
    <li v-for="(item, index) in sampleArray" :key="item">
      {{ item }} / {{ index }}
    </li>
    <li v-for="(user, index) in objArr" :key="user.id">
      {{ user }} / {{ user.id }} / {{ index }}
    </li>
  </div>
</template>

<script>
export default {
// setup(){
  data() {
    return {
      sampleArray: ['A', 'B', 'C']
      , objArr: [
        {id: 0, name: "Kim"}
        , {id: 1, name: "Lee"}
        , {id: 2, name: "Dean"}
      ]
    }
  }
}
</script>

<!--<style lang="scss" scoped>-->
<style scoped>

</style>