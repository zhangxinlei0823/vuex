<template>
  <div>
    <h3>当前最新的count值为:{{ count }}</h3>
    <button @click="sub">-1</button>
    <button @click="subN(2)">-N</button>
  </div>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import { mapState, mapMutations } from 'vuex'
export default {
  name: 'Subtraction',
  computed: {
    ...mapState(['count'])
  },
  methods: {
    ...mapMutations(['sub', 'subN'])
  }
}
</script>

<style scoped>

</style>
