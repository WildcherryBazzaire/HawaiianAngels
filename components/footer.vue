<template>
  <b-row>
    <b-col class="footer">
      <b-row align-h="center">
        <h1 class="line"></h1>
      </b-row>
      <b-row class="top" align-h="center">
        <b-col sm="1" offset-sm="1"></b-col>
        <b-col id="contact"><b>Contact</b></b-col>
        <b-col id="connect"><b>Connect</b></b-col>
      </b-row>
      <b-row align-h="center" class="mid">
        <b-col>
          <img :src="logo" />
        </b-col>
        <b-col>
          <b-row>(808)921-2747</b-row>
          <b-row>335 Merchant Street, #516 Honolulu, HI 96813</b-row>
        </b-col>
        <b-col>
          <b-row align-h="center">
            <b-col sm="2">
              <img :src="facebook" class="image-size" />
            </b-col>
            <b-col sm="2">
              <img :src="twitter" class="image-size" />
            </b-col>
          </b-row>
        </b-col>
      </b-row>
      <b-row>
        <b-col class="t-footer"
          >Copyright ©2019 Hawaii Angels, All Rights Reserved</b-col
        >
      </b-row>
      <!--
      <b-row>
        <b-col id="bottom-part"> </b-col>
      </b-row>
      -->
    </b-col>
  </b-row>
</template>

<script>
export default {
  data() {
    return {
      facebook: require('@/assets/fb.png'),
      twitter: require('@/assets/twitter2.png'),
      logo: require('@/static/logo.svg')
    }
  }
}
</script>

<style scoped>
#contact {
  right: 2.5%;
  font-size: 20px;
}
#connect {
  left: 1.5%;
  font-size: 20px;
}
.line {
  border-bottom: 3px solid #b70304;
  height: 100%;
  width: 80%;
  display: flex;
  justify-content: center;
}
.top {
  margin-top: 30px;
  margin-bottom: 25px;
}
.mid {
  margin-bottom: 30px;
}
.bottom {
  margin-bottom: 50px;
}
.footer {
  margin-top: 100px;
  width: 1200px;
  height: 250px;
}
.image-size {
  height: 50px;
}
#bottom-part {
  width: 100%;
  height: 30px;
  background-color: #640d14;
  margin-top: 9%;
}
</style>
