<template>
  <b-container id="main">
    <b-row>
      <b-col sm="12">
        <jumbotron></jumbotron>
        <h1>---Application---</h1>
        <p>
          Submit your application directly to our GUST system. Please attach an
          executive summary and full business plans to your application.
        </p>
        <b-button size="lg">Apply Here</b-button>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import jumbotron from '@/components/application/jumbotron.vue'
export default {
  components: {
    jumbotron: jumbotron
  }
}
</script>

<style></style>
