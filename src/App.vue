<script>
export default {
  data(){
    return {
      count: 0
    }
  },
  beforeCreate() {
    console.log("LifeCycle is beforeCreate :" , this.count);
  },
  created() {
    console.log("LifeCycle is created : ", this.count);
  }
}
</script>

<template>
  <div>{{count}}</div>
</template>

<style>

</style>
