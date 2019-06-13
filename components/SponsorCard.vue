<template>
  <b-col sm="12" class="mt-5">
    <b-row v-if="index % 2 === 0">
      <b-col sm="12" md="5">
        <b-img-lazy fluid center :src="content.image"></b-img-lazy>
      </b-col>
      <b-col offset-md="1" sm="12" md="6">
        <b-img
          :src="require('@/static/AlineShortRed.svg')"
          class="line-right"
        ></b-img>
        <b-img
          :src="require('@/static/AlineCurve.svg')"
          class="line-curve-right"
        ></b-img>
        <h1 class="pb-3 text-right">{{ content.title }}</h1>
        <p class="text-left" data-aos="fade-right">
          {{ content.text }}
        </p>
      </b-col>
    </b-row>
    <b-row v-else>
      <b-col sm="12" md="6">
        <b-img
          :src="require('@/static/AlineShortOrange.svg')"
          class="line-left"
        ></b-img>
        <b-img
          :src="require('@/static/AlineCurve.svg')"
          class="line-curve-left"
        ></b-img>
        <h1 class="pb-3">{{ content.title }}</h1>
        <p class="text-left" data-aos="fade-left">
          {{ content.text }}
        </p>
      </b-col>
      <b-col offset="1" sm="12" md="5">
        <b-img-lazy fluid center :src="content.image"></b-img-lazy>
      </b-col>
    </b-row>
  </b-col>
</template>

<script>
export default {
  props: {
    content: {
      default: function() {
        return {}
      },
      type: Object
    },
    index: {
      default: null,
      type: Number
    }
  }
}
</script>

<style scoped>
h1 {
  color: #b70304;
}
.text-left {
  position: relative;
}

.line-right,
.line-curve-right,
.line-left,
.line-curve-left {
  position: absolute;
}

.line-left {
  bottom: 1%;
  right: 1%;
}

.line-right {
  top: 26%;
  left: -2%;
}

.line-curve-right {
  right: -3%;
  top: -10%;
}

.line-curve-left {
  transform: rotateZ(-90deg);
  left: -3%;
  top: -6%;
}
</style>
