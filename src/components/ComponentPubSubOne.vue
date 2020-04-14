<template>
  <div>
    <h1>ComponentPubSubOne</h1>
    <input type="text" name="" id="one" v-model="pubMessage" />
    <button @click="passValuePlus">传送</button>
  </div>
</template>

<script>
import PubSub from 'pubsub-js'
export default {
  created() {},
  data() {
    return {
      pubMessage: 'default'
    }
  },
  methods: {
    passValuePlus() {
      PubSub.publish('pubMessage', this.pubMessage)
    }
  }
}
</script>

<style></style>
