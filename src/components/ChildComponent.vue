<template>
  <button @click="sendEvent">자식 컴포넌트에서 만든 버튼</button>
</template>

<script>
/*<script setup lang="ts">*/
/*import {ref} from "vue";

//반응성을 가진 타입이 String
const data = ref<String>("자식 컴포넌트에서 선언된 데이터 입니다.")
const emit = defineEmits(["send-event"]);
const sendEvent = () => {
  emit("send-event", data.value);
}*/

//options api
export default {
  data() {
    return {
      text: "자식 컴포넌트에서 선언된 데이터 입니다."
    }
  }
  , methods: {
    sendEvent() {
      this.$emit("send-event", this.text)
    }
  }
}
</script>

<style scoped>

</style>