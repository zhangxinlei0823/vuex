<template>
  <div>
<!--    <h3>{{ showNums }}</h3>-->
    <h3>{{showNums}}</h3>
    <button @click="sub">-1</button>
    <button @click="subN(2)">-N</button>
    <button @click="subAsync1">-1 Async</button>
    <button @click="subNAsync1(3)">-N Async</button>
  </div>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import { mapState, mapMutations, mapActions, mapGetters } from 'vuex'
export default {
  name: 'Subtraction',
  computed: {
    ...mapState(['count']),
    ...mapGetters(['showNums'])
  },
  methods: {
    ...mapMutations(['sub', 'subN']),
    ...mapActions(['subAsync', 'subNAsync']),
    subAsync1 () {
      // eslint-disable-next-line no-unused-expressions
      this.subAsync()
    },
    subNAsync1 (step) {
      this.subNAsync(step)
    }
  }

}
</script>

<style scoped>

</style>
