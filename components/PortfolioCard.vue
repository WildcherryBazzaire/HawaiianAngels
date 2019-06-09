<template>
  <div class="card-root-container">
    <div class="card-inner-container">
      <!-- All the lines Start here -->
      <b-img
        :src="require('@/static/Cards/aLineRed.svg')"
        class="red-line"
      ></b-img>
      <b-img
        :src="require('@/static/Cards/aLineOrange.svg')"
        class="orange-line"
      ></b-img>
      <b-img
        :src="require('@/static/Cards/aLineBlue.svg')"
        class="blue-line"
      ></b-img>
      <!-- All the line Stuff Ends Here -->
      <div
        class="card-front"
        :style="'background-image:url(' + content.image + ');'"
      ></div>
      <div class="card-back" style="text-align:center;">
        <div class="back-card-content">
          <b-row>
            <b-col sm="12">
              <p>Some Header</p>
            </b-col>
            <b-col sm="12">
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam sit
                amet elementum nisi.
              </p>
            </b-col>
            <b-col sm="12">
              <a href="#">Learn More</a>
            </b-col>
          </b-row>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    content: Object
  }
}
</script>

<style>
@keyframes minimizePicture {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(0.75);
    opacity: 0.5;
  }
  100% {
    display: none;
    opacity: 0;
    transform: scale(0.5);
  }
}
.row {
  position: absolute;
  width: 50px;
  height: 10px;
  border-radius: 50px;
}

.top {
  top: 0%;
  right: 0%;
  width: 86px;
  height: 10px;
  background-color: #b70304;
  animation: goleft 0.5s linear forwards 1s;
}

.middle {
  top: 50%;
  left: 0%;
  width: 34px;
  height: 10px;
  background-color: #de8f11;
  animation: goright 0.5s linear forwards 1s;
}

.bottom {
  bottom: 0%;
  right: -5%;
  z-index: 5;
  width: 61px;
  height: 10px;
  background-color: #56a3a6;
}

@keyframes expandContent {
  0% {
    transform: scale(0.5);
  }
  50% {
    transform: scale(0.75);
  }
  100% {
    transform: scale(1);
  }
}

@keyframes lineShiftRight {
  0% {
  }
}

/*add the keyframes */
.card-root-container {
  height: 12rem;
  width: 12rem;
  margin: auto;
}
.card-inner-container,
.card-front,
.card-back {
  width: 12rem;
  height: 12rem;
}

.card-inner-container {
  position: relative;
}

.card-front,
.card-back {
  position: absolute;
  border-radius: 0.75rem;
}

.card-front {
  background-position: center;
  background-size: cover;
  border: 1px solid black;
  z-index: 1;
  animation: expandContent 0.25s ease forwards;
}

.card-back {
  background: #4f4e4c;
  z-index: 0;
  animation: minimizePicture 0.25s ease forwards;
}

.red-line,
.orange-line,
.blue-line {
  position: absolute;
  z-index: 2;
  transition: all 0.3s ease;
}

.red-line {
  top: -2%;
  left: -24%;
}

.orange-line {
  top: 50%;
  left: -10%;
}

.blue-line {
  bottom: -2%;
  right: -9%;
}

/* .card-root-container:hover .card-back {
  animation: showContent 0.3s ease-in forwards;
} */

.card-root-container:hover .card-front {
  animation: minimizePicture 0.25s ease forwards;
}

.card-root-container:hover .card-back {
  animation: expandContent 0.25s ease forwards;
}

.card-root-container:hover .card-inner-container > .red-line {
  left: 86%;
}

.card-root-container:hover .card-inner-container > .orange-line {
  left: 90%;
}

.card-root-container:hover .card-inner-container > .blue-line {
  right: 76%;
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
