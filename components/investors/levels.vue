<template>
  <b-col sm="12" class="main-card">
    <b-row>
      <b-col>
        <b-row class="row-fix">
          <b-col md="12" offset-md="4"
            ><h2 class="h-text">{{ header }}</h2></b-col
          >
        </b-row>
        <b-row class="row-fix">
          <b-col md="12" offset-md="5">
            <h2 class="line">________</h2>
          </b-col>
        </b-row>
        <b-row class="row-fix">
          <b-col md="12" offset-md="5">
            <p class="c-text">{{ text }}</p>
          </b-col>
        </b-row>
        <b-row class="row-fix">
          <b-col md="12" offset-md="4">
            <h2>Annual Cost</h2>
          </b-col>
        </b-row>
        <b-row id="cost-t" class="row-fix">
          <b-col class="cost-t">{{ cost.headOne }}</b-col>
          <b-col class="cost-t">{{ cost.textOne }}</b-col>
          <b-col class="cost-t">{{ cost.headTwo }}</b-col>
          <b-col class="cost-t">{{ cost.textTwo }}</b-col>
        </b-row>
      </b-col>
      <b-col sm="6" class="image">
        <img :src="image" />
      </b-col>
    </b-row>
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
.image {
  position: absolute;
}
.line {
  color: red;
  height: 25px;
  position: relative;
  top: -50%;
}
.main-card {
  border: solid 1px;
  border-radius: 10px;
  box-shadow: -30px 20px #db4c40;
  height: 300px;
  margin-bottom: 5%;
  margin-top: 5%;
  max-width: 100%;
  padding: 10px;
  text-align: left;
  width: 500px;
}
</style>
