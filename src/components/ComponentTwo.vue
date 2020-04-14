<template>
  <div>
    <p>component two</p>
    <p>{{ passValue }}</p>
    <provide-inject></provide-inject>
  </div>
</template>

<script>
import Bus from '../eventBus.js'
import ProvideInject from './ProvideInject.vue'
export default {
  data() {
    return {
      passValue: 'default'
    }
  },
  components: {
    'provide-inject': ProvideInject
  },
  mounted() {
    Bus.$on('data-input', text => {
      this.passValue = text
    })
  }
}
</script>

<style></style>
