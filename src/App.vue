<template>
  <div>
    <h1>{{ text }}</h1>
    <h1>변경된 함수 호출 값 : {{ changeText() }}</h1>
    <h1>변경된 함수 호출 값 : {{ changeText() }}</h1>

    <h2>{{ computedText }}</h2>
    <h2>{{ computedText }}</h2>
  </div>
</template>

<script>
export default {
// setup(){
  data() {
    return {
      text: "Computed 테스트 데이터 문구"
    }
  },
  //methods 부분에서 선언된 함수와 동일한 로직일 때,
  // 캐싱기능이 있는 methods는 호출될 떄마다 console값이 출력
  // 반면 computed는 캐싱 기능이 없기 떄문에 methods 와 어떤 차이점이 있는지 한번 주의깊게 살펴보는 것이 포인트
  computed: {
    computedText() {
      console.log("Computed 기능")
      return this.text.split("").reverse().join('');
    }
  },
  methods: {
    changeText() {
      console.log(this.text);
      return this.text.split("").reverse().join('');
    }
  }
}
</script>

<!--<style lang="scss" scoped>-->
<style scoped>

</style>