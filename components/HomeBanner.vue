<template>
  <b-container fluid style="align-items: flex-start">
    <b-row class="banner-row">
      <b-col class="polygon" sm="7">
        <div class="polygon-content">
          <h1>OOF</h1>
          <p>Lorem Ipsum</p>
        </div>
      </b-col>
      <b-col class="banner-image" sm="6"></b-col>
    </b-row>
  </b-container>
</template>

<style scoped>
.polygon,
.banner-image {
  height: 337px;
}
.polygon {
  clip-path: polygon(0 0, 100% 0, 80% 100%, 0% 100%);
  z-index: 1;
}
.polygon-content {
  width: 80%;
  height: 100%;
}
.banner-image {
  position: absolute;
  right: 0%;
  z-index: 0;
  background-image: url('https://www.hawaiiangels.org/files/theme/banner-landing.jpg?1535600491');
  background-position: center;
  background-size: cover;
}
.banner-row {
  position: relative;
}
</style>
