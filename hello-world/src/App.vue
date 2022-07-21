<template>
  <div>{{ name }}</div>
  <div v-html="channel"></div>
  <h2 class="underline" :id="headingID">Heading</h2>
  <h3 class ="underline" :class="success">Heading 3</h3>
  <p :class="['underline', 'successClass']">New 3</p>
  <p :class="isDisabled ? 'unsuccessClass' : 'successClass' ">New 4</p>
  <h4 :class="{
    'underline': true,
    'success': isDisabled,
    'unsuccess': !isDisabled
  }">New 5</h4>
  <h2 :style="{
    color: highlightColor,
    fontSize: headerSize + 'rem'
  }">
    Inline style
  </h2>
  <button :disabled="isDisabled">Button</button>
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
      isDisabled: false,
      success: 'unsuccessClass',
      highlightColor: 'orange',
      headerSize: '20'
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
.underline{
  text-decoration: underline;
}
.successClass{
  color: green;
}
.unsuccessClass{
  color: firebrick;
}
</style>
