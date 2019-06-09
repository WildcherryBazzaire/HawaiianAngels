<template>
  <div class="card">
    <div class="top row"></div>
    <div class="middle row"></div>
    <div class="bottom row"></div>
    <div
      :style="{ zIndex: zIndexVal }"
      class="card card_front"
      @click="zIndexVal--"
    >
      <img :src="getImgUrl(logo)" />
    </div>
    <div class="card cardInfo card_back" @click="zIndexVal++">
      <h1 class="cardInfo cardTitle">{{ title }}</h1>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    title: String,
    description: String,
    logo: String
  },
  data() {
    return { zIndexVal: 3 }
  },
  methods: {
    SwitchCard: function() {
      alert('letsTalk')
    },
    getImgUrl: function(img) {
      const images = require.context('../static/images', false, /\.png$/)
      return images('./' + img + '.png')
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Ubuntu&display=swap');

#container {
  display: flex;
  flex-flow: row;
}
.row {
  position: absolute;
  width: 50px;
  height: 10px;
  border-radius: 15%;
}

.top {
  top: 0%;
  right: 0%;
  background-color: blue;
  animation: goleft 0.5s linear forwards 1s;
}

.middle {
  top: 50%;
  left: 0%;
  background-color: red;
  animation: goright 0.5s linear forwards 1s;
}

.bottom {
  bottom: 0%;
  right: -5%;
  z-index: 5;
  background-color: yellowgreen;
}

img {
  width: 257px;
  height: 256px;
}
.card {
  width: 257px;
  height: 256px;
  background: #4f4e4c;
  border-radius: 10px;
  margin: 5%;
}

.cardInfo {
  font-family: Ubuntu;
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 21px;
  display: flex;
  align-items: center;
  text-align: center;
  color: #fcfcfc;
}

.cardTitle {
  font-weight: bold;
  font-size: 28px;
}
.card_front {
  position: absolute;
  top: 0;
  z-index: 1;
}
.card_back {
  position: absolute;
  top: 0;
  z-index: 2;
}

@keyframes goleft {
  0% {
    right: 0%;
  }
  100% {
    right: 100%;
  }
}

@keyframes goright {
  0% {
    left: 0%;
  }
  100% {
    left: 100%;
  }
}
</style>
