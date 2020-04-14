<template>
  <div>
    <p>component one</p>
    <input type="text" name="" id="one" v-model="inputText" />
    <button @click="passValue">传送</button>
  </div>
</template>

<script>
import Bus from '../eventBus.js'
export default {
  data() {
    return {
      inputText: 'default'
    }
  },
  methods: {
    passValue() {
      Bus.$emit('data-input', this.inputText)
    }
  }
}
</script>

<style></style>
