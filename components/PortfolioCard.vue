<template>
  <div class="card">
    <div
      :style="{ zIndex: zIndexVal }"
      class="card card_front"
      @click="zIndexVal--"
    >
      <img :src="logo" />
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

.card {
  width: 257px;
  height: 256px;
  background: #4f4e4c;
  border-radius: 10px;
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
</style>
