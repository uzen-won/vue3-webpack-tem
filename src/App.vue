<template>
  <h1 @click="increase">{{ count }}</h1>
  <div v-if="count > 4">4보다 큽니다!</div>
  <ul>
    <Fruit v-for="fruit in fruits" :key="fruit" :name="fruit">
      {{ fruit }}
    </Fruit>
  </ul>
</template>  

<script>
import Fruit from '~/components/Fruit'

export default {
  components: { //import 등록
    //Fruit: Fruit   객체데이터 내부에서 속성이름과 데이터의 이름이 같으면 :뒤쪽 생략 가능
    Fruit
  },
  data() {
    return {
      count: 0,
      fruits: [
        'Apple', 'Banana', 'Cherry'
      ]
    }
  },
  methods: {
    increase() { //함수
      this.count += 1 //this = script
    }
  }
}
</script>

<style lang="scss">
h1 {
  font-size: 50px;
  color: royalblue;
  cursor: pointer;
}
</style>