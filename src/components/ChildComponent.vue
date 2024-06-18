<template>
  <div>{{ sendProps1 }}</div>
  <div>{{ sendProps2 }}</div>
  <div>{{ sendProps3.id }} / {{ sendProps3.name }}</div>
</template>

<script setup lang="ts">
// 1. 컴포넌트api에서 타입스크립트로 활용하는 방법
// 1-1 prop 받은 데이터 형식에 맞게 타입을 지정해준다.

//import {defineProps} from 'vue'
//prop 받은 데이터 이름 자체에 미리 선언해둔 타입을 설정해준다.


import {toRefs} from "vue";

interface Props {
  sendProps1: String,
  sendProps2: Number,
  sendProps3: Obj
}

// defineProps toRefs 내장함수를 통해 prop 받은 데이터를 활용하여 템플릿 부분에 호출하여 사용한다.
interface Obj {
  id: Number,
  name: String
}


const props = defineProps<Props>();

// 객체 구조 분해를 통해 활용
const {sendProps1, sendProps2, sendProps3} = toRefs(props);


/*export default {
  name: "ChildComponent"
  , props: {
    sendProps1: String
    , sendProps2: Number
    , sendProps3: Object
  }
  , data() {
    return {}
  }
}*/
</script>

<style scoped>

</style>