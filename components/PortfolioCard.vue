<template>
  <div class="card-root-container">
    <div class="card-inner-container">
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
}

.card-back {
  background: #4f4e4c;
  z-index: 0;
}

/* .card-root-container:hover .card-back {
  animation: showContent 0.3s ease-in forwards;
} */

.card-root-container:hover .card-front {
  animation: minimizePicture 0.25s ease-in forwards;
}
</style>
