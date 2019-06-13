<template>
  <b-card>
    <b-img
      :src="require('@/static/AlineCurvePointBlue.svg')"
      class="corner-line"
    ></b-img>
    <b-img
      :src="require('@/static/AlineShortOrange.svg')"
      class="bottom-line"
    ></b-img>
    <slot></slot>
  </b-card>
</template>

<style scoped>
.card {
  position: relative;
  border-radius: 0rem;
  border: none;
  background: rgba(0, 0, 0, 0);
  z-index: 1;
}

.card-body {
  height: 12.25rem;
}

.card::before {
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(255, 146, 137, 0.5);
  top: -1rem;
  right: 4px;
  bottom: 0;
  left: 0.975rem;
  z-index: 0;
  content: '';
}

.card-title {
  color: #db4c40;
}

.card-text {
  color: #4f4e4c;
}

.corner-line,
.bottom-line {
  position: absolute;
}

.corner-line {
  top: 0%;
  left: 0%;
}

.bottom-line {
  bottom: 0%;
  right: 0%;
}
</style>
