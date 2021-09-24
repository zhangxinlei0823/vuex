<template>
  <div>
    <my-addition></my-addition>

    <p>--------------------------</p>

    <my-subtraction></my-subtraction>
  </div>
</template>

<script>
import Addition from '@/components/Addition'
import Subtraction from '@/components/Subtraction'
export default {
  data () {
    return {}
  },
  components: {
    // eslint-disable-next-line vue/no-unused-components
    'my-addition': Addition,
    // eslint-disable-next-line vue/no-unused-components
    'my-subtraction': Subtraction
  }
}
</script>
