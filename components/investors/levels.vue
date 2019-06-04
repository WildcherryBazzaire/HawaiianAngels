<template>
  <b-col sm="12" class="main-card">
    <h1>{{ header }}</h1>
  </b-col>
</template>

<script>
export default {
  props: {
    header: String
  }
}
</script>

<style>
.main-card {
  border: solid 1px;
  border-radius: 10px;
  box-shadow: 20px 20px #db4c40;
  height: 300px;
  margin-top: 5%;
  margin-bottom: 5%;
  padding: 10px;
  width: 500px;
}
</style>
