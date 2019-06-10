<template>
  <b-col sm="12" class="page-headers py-4">
    <!--This column is the header for the stuff -->
    <span class="lines"></span>
    <span class="text-sm-center">
      <h1 style="font-size:48px;color:#b70304;">{{ content }}</h1>
      <p class="ma-0" v-if="additionalContent">
        {{ additionalContent }}
      </p>
    </span>
    <span class="lines"></span>
  </b-col>
</template>

<script>
export default {
  props: {
    content: String,
    additionalContent: String
  }
}
</script>

<style scoped>
.lines {
  margin: auto 1rem;
  width: 53px;
  padding-top: 5px;
  border-bottom: 0.25px solid #6cd4ff;
}
.page-headers {
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
}
</style>
