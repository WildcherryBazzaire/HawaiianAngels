<template>
  <b-row align-h="end">
    <b-col>
      <img :src="content[0].image" />
      <h2 class="h-plan-name">{{ content[0].planName }}</h2>
      <b-card class="box">
        <p>- Refresh your yearly plan</p>
        <p>- Save $50 off</p>

        <b-button class="b-choose-this-plan" @click="openReoccuring()"
          >Choose this Plan</b-button
        >
      </b-card>
    </b-col>
    <div class="divider"></div>
    <b-col>
      <img :src="content[1].image" />
      <h2 class="h-plan-name">{{ content[1].planName }}</h2>
      <b-card class="box">
        <p>- Refresh your yearly plan</p>
        <p>- Save $50 off</p>
        <b-button
          class="b-choose-this-plan"
          @click="
            openOneTime()
            openReoccuring()
          "
          >Choose this Plan</b-button
        >
      </b-card>
    </b-col>
  </b-row>
</template>

<script>
// import bus from '@/components/investors/bus'
export default {
  data() {
    return {
      oneTime: false,
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
  methods: {
    openReoccuring: function() {
      this.$emit('changeDisplay', true)
    },
    openOneTime: function() {
      this.$emit('asetActive', true)
    }
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
