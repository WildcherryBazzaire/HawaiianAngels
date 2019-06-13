<template>
  <b-col>
    <b-row>
      <Category-Header :content="'Contact Us'" />
    </b-row>
    <b-row align-h="center">
      <b-row id="contact-us-container">
        <b-col sm="6" class="top-content">
          <b-row align-h="center">
            <b-col class="over">
              <b-row align-h="center"><h2>Stay in Touch</h2></b-row>
              <b-row>
                <b-col offset-sm="1">We Can't Wait to Hear From You!</b-col>
              </b-row>
              <b-row class="left-side">
                <b-col offset-sm="2"
                  ><img :src="phone" :style="{ height: '50px' }"
                /></b-col>
                <b-col sm="8" offset-sm="12">(808)921-2747</b-col>
              </b-row>
              <b-row class="left-side">
                <b-col offset-sm="2"
                  ><img :src="address" :style="{ height: '50px' }"
                /></b-col>
                <b-col sm="8" offset-sm="12"
                  >335 Merchant Street, #516 Honolulu, HI 96813</b-col
                >
              </b-row>
              <b-row>
                <b-col offset-sm="1">Social Media</b-col>
              </b-row>
            </b-col>
          </b-row>
          <div
            :style="{
              'background-image': ' url(' + image + ')',
              'background-size': '1100px',
              'background-repeat': 'no-repeat',
              'background-position': 'center',
              opacity: '0.2',
              postion: 'relative',
              'z-index': '-1',
              width: '100%',
              height: '100%'
            }"
          ></div>
        </b-col>
        <b-col sm="6" :style="{ 'background-color': '#b70304' }">
          <b-row
            class="right-side"
            align-h="center"
            :style="{ 'margin-top': '10%' }"
          >
            <b-form-input placeholder="Name" class="form-field"></b-form-input>
          </b-row>
          <b-row class="right-side" align-h="center">
            <b-form-input placeholder="Email" class="form-field"></b-form-input>
          </b-row>
          <b-row class="right-side" align-h="center">
            <b-form-textarea
              placeholder="Comment"
              class="form-field-lrg"
              rows="8"
            >
            </b-form-textarea>
          </b-row>
          <b-row align-h="center" :style="{ 'margin-top': '10%' }">
            <b-button class="sub-btn">Submit</b-button>
          </b-row>
        </b-col>
      </b-row>
    </b-row>
  </b-col>
</template>

<script>
import CategoryHeader from '@/components/CategoryHeader'
export default {
  components: {
    'Category-Header': CategoryHeader
  },
  data() {
    return {
      image: require('@/assets/contact-us/map.png'),
      phone: require('@/assets/contact-us/phone.svg'),
      address: require('@/assets/contact-us/address.svg')
    }
  }
}
</script>

<style>
#contact-us-container {
  overflow: hidden;
  border: transparent 1px;
  border-radius: 50px;
  width: 60%;
  height: 600px;
}
.left-side {
  margin-top: 5%;
  margin-bottom: 5%;
}
.top-content {
  position: relative;
  z-index: 1;
  padding-right: 0;
}
.oof {
  position: relative;
  z-index: 5;
}
.over {
  position: absolute;
  z-index: 5;
  font-weight: bold;
  margin-top: 20px;
}
.right-side {
  margin-top: 5%;
}
.form-field {
  width: 75%;
  height: 60px;
  background-color: transparent;
}
.form-field-lrg {
  width: 75%;
  background-color: transparent;
}
::placeholder {
  color: white;
  opacity: 1;
}
.sub-btn {
  background-color: #de8f11;
  width: 75%;
}
</style>
