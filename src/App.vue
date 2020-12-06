<template>
  <div id="app">
    <GitBranch />
  </div>
</template>

<script>
import GitBranch from "@/components/GitBranch";

export default {
  name: 'App',
  components: {
    GitBranch,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
