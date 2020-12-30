<template>
  <div>
    <h1>Portfólio</h1>

    <ul>
      <li v-for="portfolio in portfolios" :key="portfolio">
        <img :src="portfolio.image" alt="">
      </li>
    </ul>
  </div>
</template>

<script>
import portfoliosQuery from '~/apollo/queries/portfolio/portfolios.gql'

export default {
  data() {
    return {
      api_url: process.env.strapiBaseUri,
      portfolios: []
    }
  },
  apollo: {
    portfolios: {
      prefetch: true,
      query: portfoliosQuery,
      variables () {
        return { id: parseInt(this.$route.params.id) }
      }
    }
  }

}
</script>
<style lang="scss">

</style>
