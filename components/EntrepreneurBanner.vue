<template>
  <b-jumbotron fluid :header="content"> </b-jumbotron>
</template>

<script>
export default {
  props: {
    content: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
.jumbotron {
  background: url('https://www.hawaiiangels.org/uploads/2/3/4/9/23499640/2432007_orig.jpg');
  background-position: center;
  background-size: cover;
}

h1 {
  text-align: center;
  font-size: 48px;
  background: rgba(0, 0, 0, 0.3);
  border-radius: 1rem;
  padding: 5rem 0;
  color: #fcfcfc;
  font-weight: normal;
}
</style>
