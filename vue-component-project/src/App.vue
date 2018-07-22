<template>
  <div id="app">
    <button v-on:click="selectedComponent = 'app-red'">Select Red Component</button>
    <button v-on:click="selectedComponent = 'app-green'">Select Green Component</button>
    <button v-on:click="selectedComponent = 'app-blue'">Select Blue Component</button>

    <keep-alive>
      <component v-bind:is="selectedComponent"><p>hehe, she said 'SLOTS'</p></component>
    </keep-alive>
    </div>
</template>

<script>

import Blue from './components/blue.vue'
import Green from './components/green.vue'
import Red from './components/red.vue'

export default {
  name: 'App',
  data: function () {
    return {
      selectedComponent: ''
    }
  },
  components: {
    'app-blue': Blue,
    'app-green': Green,
    'app-red': Red
  }
}
</script>

<style scoped>
  div {
    padding: 30px;
    background-color: #c0c0c0;
  }
</style>
