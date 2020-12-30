<template>
  <div class="mb-16">
    <nuxt-link to="/portfolio">Portfólio</nuxt-link>
  </div>
</template>

<script>
import portfoliosQuery from '~/apollo/queries/portfolio/portfolios.gql'

export default {
  data() {
    return {
      portfolios: []
    }
  },
  components: {
  },

}
</script>

<style lang="scss">
</style>
