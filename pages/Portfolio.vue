<template>
  <div id="cont">
    <Card />
    <Card />
    <Card />
  </div>
</template>

<script>
import Card from '../components/PortfolioCard.vue'

export default {
  components: {
    Card
  }
}
</script>

<style>
#cont {
  display: flex;
  flex-flow: row wrap;
}
</style>
