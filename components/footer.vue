<template>
  <b-row>
    <b-col class="footer">
      <b-row>
        <b-col class="t-footer" :style="{ 'font-size': '36px' }"
          >Follow us on</b-col
        >
      </b-row>
      <b-row align-h="center">
        <b-col> <img :src="logo"/></b-col>
        <b-col
          ><img :src="facebook" :style="{ height: '50px' }"/>
          <img :src="twitter" :style="{ height: '50px' }"
        /></b-col>
        <b-col>
          <b-row class="t-footer">Phone: (808)921-2747</b-row>
          <b-row class="t-footer"
            >Address: 335 Merchant Street, #516 Honolulu, HI 96813
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
      facebook: require('@/assets/contact-us/facebook.png'),
      twitter: require('@/assets/contact-us/twiiter.png'),
      logo: require('@/static/logo.svg')
    }
  }
}
</script>

<style>
.t-footer {
  color: white;
}
.footer {
  width: 1200px;
  height: 200px;
  background-color: #b70304;
}
#bottom-part {
  width: 100%;
  height: 30px;
  background-color: #640d14;
  margin-top: 9%;
}
</style>
