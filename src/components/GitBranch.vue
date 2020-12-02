<template>
  <div>
    <h1>{{ greeting }}</h1>
    <button>
      <h3>Push to origin/{{ branch }}</h3>
    </button>
  </div>
</template>

<script>

import {FEATURES} from "@/featureToggler";

const withCovid = base => {
  if (FEATURES.COVID) {
    return {
      extends: base,
      data: () => ({
        greeting: 'BE SAFE!'
      })
    };
  }
  return base;
};

const withHumanRights = base => {
  if (FEATURES.HUMAN_RIGHTS) {
    return {
      extends: base,
      props: {
        branch: {
          type: String,
          default: 'main'
        }
      },
    };
  }
  return base;
}

export default withCovid(withHumanRights({
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
}))
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
