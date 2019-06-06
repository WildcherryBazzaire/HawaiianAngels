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
        <button class="button">Apply Here</button>
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

<style>
.button {
  background-color: #de8f11;
  color: #fcfcfc;
  border-radius: 10px;
}
</style>
