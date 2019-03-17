<template>
  <div id="app">
    <HelloWorld title="slot">
      <p class="etc">Begin!</p>
      <p class="inner" slot="a">***First message***</p>
      <p class="etc">Middle...</p>
      <p class="inner" slot="b">***Second message***</p>
      <p class="etc">End.</p>
      <p class="inner" slot="c">***Third message***</p>
    </HelloWorld>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
