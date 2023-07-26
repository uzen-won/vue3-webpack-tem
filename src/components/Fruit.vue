<template>
  <li>{{name}}?!</li>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      default : ''
    }
  },
  data() {
    return {

    }
  }
}
</script>

<style scoped lang="scss"> //scoped -> 다른 컵포넌트에 적용x 유효범위를 제한함. 현재 컴포넌트 내에서만 적용
  h1 {
    color: red!important;
  }
</style>