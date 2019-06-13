<template>
  <b-row align-h="center">
    <b-col>
      <b-row v-if="propOneTime === true" class="oneTime" align-h="center">
        <img :src="content[1].image" />
        <h2 class="h-plan-name">{{ content[1].planName }}</h2>
      </b-row>
      <b-row v-if="propReoccuring === true" class="reoccuring" align-h="center">
        <img :src="content[0].image" />
        <h2 class="h-plan-name">{{ content[0].planName }}</h2>
      </b-row>
    </b-col>
    <b-row align-h="center">
      <div class="divider"></div>
    </b-row>
    <b-col v-if="propOneTime === true">
      <b-row align-h="center">
        <h3>One Time Stuff</h3>
      </b-row>
    </b-col>
    <b-col v-if="propReoccuring === true">
      <b-row align-h="center">
        <h3>This is for reoccuring</h3>
      </b-row>
    </b-col>
  </b-row>
</template>

<script>
// import bus from '@/components/investors/bus'
export default {
  props: {
    propOneTime: Boolean,
    propReoccuring: Boolean
  },
  data() {
    return {
      content: [
        {
          planName: 'Reoccuring',
          image: require('@/assets/investors/reoccuring.svg')
        },
        {
          planName: 'One Time',
          image: require('@/assets/investors/one_time.svg')
        }
      ]
    }
  },
  created() {
    this.$bus.$on('planChanged', function(oneTime) {
      this.setActiveOneTime = oneTime
      // eslint-disable-next-line
        console.log(this.oneTime)
      // eslint-disable-next-line
        console.log(this.setActiveOneTime)
    })
  }
}
</script>

<style>
.b-choose-this-plan {
  background-color: #de8f11;
  border-radius: 20px;
  height: 40px;
  width: 150px;
}
.h-plan-name {
  color: #de8f11;
}
.h-plan-options {
  color: #56a3a6;
}
#main-choose-this-plan {
  align-items: center;
  display: flex;
}
</style>
