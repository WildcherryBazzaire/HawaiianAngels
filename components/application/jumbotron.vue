<template>
  <b-row>
    <b-col
      class="jumbotron"
      :style="{
        'background-image':
          'url(' + require('@/assets/application/jumbotron.svg') + ')'
      }"
    >
      <b-row align-h="center">
        <h1 class="h-text">
          Hawaii's Top Investors at the Tip of your Fingertips
        </h1>
      </b-row>
    </b-col>
  </b-row>
</template>

<style>
.jumbotron {
  background-repeat: no-repeat;
  background-size: cover;
  height: 500px;
  width: 100%;
  width: 100vw;
}
.h-text {
  color: white;
  font-size: 48px;
}
</style>
