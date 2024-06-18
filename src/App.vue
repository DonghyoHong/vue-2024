<template>
  <div>
    <ChildComponent
        v-bind:sendProps1="title"
        v-bind:sendProps2="year"
        :sendProps3="obj"
    ></ChildComponent>
  </div>
</template>

<script setup lang="ts">
//composition APi형태
import ChildComponent from "@/components/ChildComponent.vue";
import {reactive, ref} from "vue";

interface Obj {
  id: Number,
  name: String
}

const title = ref<string>("부모 컴포넌트에서 선언된 데이터입니다.");
const year = ref<number>(2024);
const obj = reactive<Obj>({
  id: 2024
  , name: "John"
});

// Opntion API 형태
/*export default {
// setup(){
  data() {
    return {
      title: "부모 컴포넌트에서 선언된 데이터입니다."
      , year: 2024
      , obj: {
        id: 2024
        , name: "John"
      }
    }
  }
  , components: {
    ChildComponent
  }
}*/
</script>

<!--<style lang="scss" scoped>-->
<style scoped>

</style>