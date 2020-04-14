<template>
  <div id="app">
    <component-one></component-one>
    <component-two></component-two>

    <component-pubsub-one></component-pubsub-one>
    <component-pubsub-two></component-pubsub-two>
  </div>
</template>

<script>
import ComponentOne from './components/ComponentOne.vue'
import ComponentTwo from './components/ComponentTwo.vue'
import ComponentPubSubOne from './components/ComponentPubSubOne.vue'
import ComponentPubSubTwo from './components/ComponentPubSubTwo.vue'
// import Bus from './eventBus.js'

export default {
  name: 'App',
  provide: {
    name: 'provide-inject传输'
  },
  components: {
    'component-one': ComponentOne,
    'component-two': ComponentTwo,
    'component-pubsub-one': ComponentPubSubOne,
    'component-pubsub-two': ComponentPubSubTwo
  }
}
</script>

<style></style>
