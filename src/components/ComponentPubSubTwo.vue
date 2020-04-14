<template>
  <div>
    <h1>ComponentPubSubTwo</h1>
    <p>{{ pubMessage }}</p>
  </div>
</template>

<script>
import PubSub from 'pubsub-js'
export default {
  created() {
    PubSub.subscribe('pubMessage', (msg, pubMessage) => {
      console.log(pubMessage)
      console.log(msg)
      this.pubMessage = pubMessage
    })
  },
  data() {
    return {
      pubMessage: 'pubsub'
    }
  }
}
</script>

<style></style>
