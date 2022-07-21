<template>
  <div>{{ name }}</div>
  <div v-html="channel"></div>
  <h2 v-bind:id="headingID">Heading</h2>
  <button v-bind:disabled="isDisabled">Button</button>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return {
      name: 'Hello World',
      channel: '<span>Channel</span>',
      headingID: 'heading',
      isDisabled: true
    }
  },
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #1e7ddb;
  margin-top: 60px;
}
</style>
