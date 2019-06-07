<template>
  <div class="card">
    <div
      :style="{ zIndex: zIndexVal }"
      class="card card_front"
      @click="zIndexVal--"
    >
      <img
        src="https://www.hawaiiangels.org/uploads/2/3/4/9/23499640/174235.png?319"
      />
    </div>
    <div class="card cardInfo card_back" @click="zIndexVal++">
      <h1 class="cardInfo cardTitle">neuralink</h1>
      <p>
        Neural Analytics (NA) is developing a product that will allow
        physicians, first responders and even laypeople to accurately and
        quickly determine the severity of brain trauma in the field. Our device
        will simplify brain injury diagnosis, reduce healthcare costs and
        improve patient outcomes.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
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
