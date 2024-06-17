<template>
  <button v-on:click="changeMessage">
    {{ message }}
  </button>
  {{ watchMessage }}
</template>

<script>
export default {
// setup(){
  data() {
    return {
      message: "안녕하세요. Vue.js Match 기능 테스트 오리지널 문구"
      , watchMessage: ''
    }
  },
  methods: {
    changeMessage() {
      console.log("함수 호출");
      this.message = "변경된 메세지 입니다.";
    }
  },
  watch: {
    //데이터 뿐만 아니라 Computed로 계산된 형태의 데이터도 Watch로 감지할 수 있다.
    // 보통 게시판에서 한 컬럼을 선택하였을 때 고유한 id값이 변경됨을 감지하고
    // 이떄 그 id값에 따른 상세 데이터를 호출할 때 주로 사용된다.
    message() {
      //alert("메세지 변수에 담긴 데이터가 변경되었습니다.");
      this.watchMessage = "Watch 동작";
    },
    id() {
      //해당 상세 데이터를 조회하는 api를 호출
    }
  }
}
</script>

<!--<style lang="scss" scoped>-->
<style scoped>

</style>