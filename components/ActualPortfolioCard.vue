<template>
  <b-col sm="12" md="7" lg="6">
    <b-row v-if="position % 2 == 0">
      <b-col sm="4" class="portfolio-container">
        <b-img class="portfolio-image" :src="content.image" fluid></b-img>
      </b-col>
      <b-col sm="8">
        <b-row>
          <b-col sm="12" class="pb-2 header-content pl-0">
            <h1 class="card-title">{{ content.name }}</h1>
            <b-img
              :src="require('@/static/AlineThree.svg')"
              class="line-threeway-left"
            ></b-img>
          </b-col>
          <b-col sm="12" class="pl-5 text-container">
            <p style="font-size:12px;" class="pr-2">
              {{ content.text }}
            </p>
            <b-img
              :src="require('@/static/AlineCurveFlipped.svg')"
              class="line-curve-left"
            ></b-img>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    <b-row v-else>
      <b-col sm="8" class="container-right">
        <b-img
          :src="require('@/static/AlineThreeReverse.svg')"
          class="line-threeway-right"
        ></b-img>
        <b-row>
          <b-col sm="12" class="pb-2 header-content pl-0">
            <h1 class="card-title">{{ content.name }}</h1>
          </b-col>
          <b-col sm="12" class="pl-2 text-container">
            <p style="font-size:12px;" class="pl-2">
              {{ content.text }}
            </p>
          </b-col>
        </b-row>
      </b-col>
      <b-col sm="4" class="portfolio-container">
        <b-img
          :src="require('@/static/AlineCurveTrans.svg')"
          class="line-curve-right"
        ></b-img>
        <b-img class="portfolio-image" :src="content.image" fluid></b-img>
      </b-col>
    </b-row>
  </b-col>
</template>

<script>
export default {
  props: {
    position: {
      default: null,
      type: Number
    },
    content: {
      default: function() {
        return {}
      },
      type: Object
    }
  }
}
</script>

<style scoped>
.card-title {
  color: #b70304;
}

.text-container > p {
  height: 196px;
}
.portfolio-container {
  position: relative;
  display: inline-flex;
  justify-content: center;
  align-items: center;
}
.portfolio-image {
  border-radius: 0.625rem;
  box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.25);
}

.text-container,
.header-content,
.container-right {
  position: relative;
}

.line-curve-left,
.line-threeway-left,
.line-curve-right,
.line-threeway-right {
  position: absolute;
}

.line-curve-right,
.line-curve-left {
  height: 2rem;
}

.line-threeway-left,
.line-threeway-right {
  height: 2rem;
}

.line-threeway-left {
  top: 80%;
}

.line-threeway-right {
  bottom: 0%;
  left: -11%;
}

.line-curve-left {
  right: 6%;
  bottom: 8%;
}

.line-curve-right {
  top: 0%;
  right: 0%;
}
</style>
