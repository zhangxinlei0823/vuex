<template>
  <div>
    <h3>当前最新的count值为:{{$store.state.count}}</h3>
    <button @click="btnHandler()">+1</button>
  </div>
</template>

<script>
export default {
  name: 'Addition',
  // eslint-disable-next-line no-labels
  methods: {
    // eslint-disable-next-line no-unused-vars,no-inner-declarations
    btnHandler () {
      this.$store.commit('add')
    }
  }
}

</script>

<style scoped>

</style>
