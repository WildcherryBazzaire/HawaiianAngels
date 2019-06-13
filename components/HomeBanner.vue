<template>
  <b-container fluid style="align-items: flex-start">
    <b-row class="banner-row">
      <b-col class="polygon" sm="8">
        <b-container class="polygon-content">
          <b-row>
            <b-col sm="12">
              <p style="font-size:24px;width: 80%; font-weight:lighter;">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam
                iaculis dolor non lacus pulvinar interdum. In blandit, massa eu
                tincidunt dapibus, lorem tortor mattis leo, sit amet vehicula
              </p>
            </b-col>
            <b-col>
              <b-button
                class="btn-warning text-white"
                size="md"
                to="/entrepreneurs"
                >Pitch the Angels</b-button
              >
            </b-col>
          </b-row>
        </b-container>
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
  background: #fcfcfc;
  clip-path: polygon(0 0, 100% 0, 80% 100%, 0% 100%);
  z-index: 1;
  background: #b70304;
}
.polygon-content {
  width: 80%;
  height: 100%;
  min-height: 0;
  align-items: start;
  padding-top: 4rem;
  justify-content: flex-start;
  text-align: initial;
  color: #fcfcfc;
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
