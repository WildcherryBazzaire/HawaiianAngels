<template>
  <b-row align-h="end">
    <b-col>
      <div class="oneTime">
        <img :src="content[1].image" />
        <h2 class="h-plan-name">{{ content[1].planName }}</h2>
      </div>
      <div>
        <img :src="content[0].image" />
        <h2 class="h-plan-name">{{ content[0].planName }}</h2>
      </div>
    </b-col>
    <div class="divider"></div>
    <b-col v-if="setActiveOneTime === true">
      <div>
        <h3>IT WORKS WOOMIES FOR EVERYONE!!!</h3>
      </div>
      <div>
        <h3>This is for reoccurintg</h3>
      </div>
    </b-col>
  </b-row>
</template>

<script>
// import bus from '@/components/investors/bus'
export default {
  props: {
    setActiveOneTime: Boolean
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
  margin-top: 100px;
}
#main-choose-this-plan {
  align-items: center;
  display: flex;
}
</style>
