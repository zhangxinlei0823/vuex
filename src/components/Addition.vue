<template>
  <div>
    <h3>当前最新的count值为:{{$store.state.count}}</h3>
    <button @click="btnHandler1()">+1</button>
    <button @click="btnHandler2()">+N</button>
    <button @click="btnHandler3()">+1 Async</button>
    <button @click="btnHandler4(3)">+N Async</button>
  </div>
</template>

<script>
export default {
  name: 'Addition',
  // eslint-disable-next-line no-labels
  methods: {
    // eslint-disable-next-line no-unused-vars,no-inner-declarations
    btnHandler1 () {
      this.$store.commit('add')
    },
    btnHandler2 () {
      this.$store.commit('addN', 3)
    },
    btnHandler3 () {
      this.$store.dispatch('addAsync')
    },
    btnHandler4 (step) {
      this.$store.dispatch('addNAsync', step)
    }
  }
}

</script>

<style scoped>

</style>
