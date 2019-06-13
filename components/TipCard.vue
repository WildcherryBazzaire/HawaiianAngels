<template>
  <b-card
    :img-src="require('@/static/Entrepreneurs/tools.png')"
    no-body
    img-bottom
  >
    <b-card-title class="card-title">
      <p class="my-0 h1">Tips</p>
      <p class="h4 py-0">For Presentors</p>
      <b-img :src="require('static/AlineShortOrange.svg')"></b-img>
    </b-card-title>
  </b-card>
</template>

<style scoped>
.card-title {
  position: relative;
}

.card-title > p {
  color: #de8f11;
}

.card {
  border: none;
  z-index: 1;
}

.card::before {
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(222, 143, 17, 0.5);
  top: -1rem;
  right: 4px;
  bottom: 0;
  left: 0.975rem;
  z-index: 0;
  content: '';
}

.card-img-bottom {
  z-index: 2;
}
</style>
