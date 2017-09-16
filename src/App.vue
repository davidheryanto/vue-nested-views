<template>
  <div id="app">
    <p>For the same property, values set by parent will override values in child</p>
    <router-view></router-view>
  </div>
</template>

<script>

import Parent from '@/components/Parent'

export default {
  name: 'app',
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
