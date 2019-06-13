<template>
  <div class="card-root-container mx-auto">
    <div class="card-inner-container">
      <div
        class="card-front"
        :style="'background-image:url(' + content.image + ');'"
      ></div>
      <b-container class="card-back" style="text-align:center;" fluid>
        <b-row>
          <b-col sm="12">
            <p class="h4">{{ content.name }}</p>
          </b-col>
          <b-col sm="12">
            <p>{{ content.text }}</p>
          </b-col>
          <b-col sm="12">
            <a href="#">Learn More</a>
          </b-col>
        </b-row>
      </b-container>
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

<style scoped>
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

p {
  color: #fcfcfc;
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

.card-back {
  text-align: center;
  align-items: center;
  justify-content: center;
  display: flex;
  width: 100%;
  height: 100%;
  margin: auto;
}

/*add the keyframes */
.card-root-container {
  height: 16rem;
  width: 16rem;
  margin: 2%;
}
.card-inner-container,
.card-front {
  width: 16rem;
  height: 16rem;
  overflow: hidden;
}

.card-inner-container::before {
  position: absolute;
  top: -0.625rem;
  right: -0.625rem;
  bottom: -0.625rem;
  left: -0.625rem;
  transform: rotate(45deg);
  content: '';
  border: inherit;
  transform: rotate(45deg);
  border-radius: 0.625rem;
  z-index: 2;
}

.card-inner-container {
  position: relative;
  -webkit-clip-path: polygon(
    30% 0%,
    70% 0%,
    100% 30%,
    100% 70%,
    70% 100%,
    30% 100%,
    0% 70%,
    0% 30%
  );
  clip-path: polygon(
    30% 0%,
    70% 0%,
    100% 30%,
    100% 70%,
    70% 100%,
    30% 100%,
    0% 70%,
    0% 30%
  );
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  overflow: hidden;
  border: 0.625rem solid #56a3a6;
  border-radius: 0.625rem;
}

.card-front,
.card-back {
  position: absolute;
  border-radius: 0.75rem;
}

.card-front {
  background-position: center;
  background-size: cover;
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
    left: 100;
  }
}
</style>
