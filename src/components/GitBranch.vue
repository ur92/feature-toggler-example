<template>
  <div>
    <h1>{{ greeting }}</h1>
    <button>
      <h3>Push to origin/{{ branch }}</h3>
    </button>
  </div>
</template>

<script>
export default {
  name: 'GitBranch',
  props: {
    branch: {
      type: String,
      default: 'master'
    }
  },
  data: () => ({
    greeting: 'LIQUEFY YOUR FRONTEND VERSION'
  })
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
