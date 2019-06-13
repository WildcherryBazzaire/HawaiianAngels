<template>
  <b-col sm="4" class="cursed">
    <div class="main-card">
      <b-row>
        <b-col sm="6" class="image">
          <img class="image-size" :src="image" />
        </b-col>
      </b-row>
    </div>
    <div class="custom-box-shadow"></div>
  </b-col>
</template>

<script>
export default {
  props: {
    header: String,
    text: String,
    cost: Object,
    image: String
  }
}
</script>

<style>
.c-text {
  max-width: 600px;
  font-size: 20px;
}
.h-text {
  font-size: 65px;
  margin: 0px 0px 0px;
  max-width: 500px;
}
#cost-t {
  margin-left: 465px;
}
.cost-t {
  max-width: 150px;
}
.cursed {
  max-height: 500px;
}
.custom-box-shadow {
  background-image: radial-gradient(#ff6961 20%, transparent 0),
    radial-gradient(#ff6961 20%, transparent 0);
  background-size: 24px 24px;
  background-position: 0 0, 12px 12px;
  border: transparent 1px;
  border-radius: 10px;
  height: 450px;
  right: 15%;
  margin-bottom: 2%;
  margin-left: 2%;
  margin-right: 2%;
  margin-top: 2%;
  padding: 10px;
  position: relative;
  text-align: left;
  bottom: 80%;
  width: 330px;
  z-index: 2;
}
.image {
  position: absolute;
}
.image-size {
  height: 100px;
}
.line {
  color: red;
  height: 25px;
  position: relative;
  top: -50%;
}
.main-card {
  background-color: white;
  border: solid 1px;
  border-radius: 10px;
  height: 450px;
  margin-bottom: 2%;
  margin-left: 2%;
  margin-right: 2%;
  margin-top: 2%;
  padding: 10px;
  position: relative;
  text-align: left;
  width: 300px;
  z-index: 5;
}
</style>
