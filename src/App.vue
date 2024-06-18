<template>
  <div>
    부모 컴포넌트 Layout
    <ChildComponent @send-event="parentEvent"></ChildComponent>
  </div>
</template>

<script>
import ChildComponent from "@/components/ChildComponent.vue";

export default {
  components: {
    ChildComponent
  }
  , methods: {
    parentEvent(event) {
      console.log(event);
    }
  }
}

//composition APi형태
/*

const parentEvent = (event: string) => {
  console.log(event);
}*/
</script>

<!--<style lang="scss" scoped>-->
<style scoped>

</style>