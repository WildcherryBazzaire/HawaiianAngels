<template>
  <b-row align-h="end">
    <b-col>
      <h2>{{ content[0].planName }}</h2>
      <img :src="content[0].image" />
      <div class="box">
        <p>- Refresh your yearly plan</p>
        <p>- Save $50 off</p>
        <div id="main-choose-this-plan">
          <div class="b-choose-this-plan">Choose this Plan</div>
        </div>
      </div>
    </b-col>
    <div class="divider"></div>
    <b-col>
      <h2>{{ content[1].planName }}</h2>
      <img :src="content[1].image" />
      <div class="box">
        <p>- Refresh your yearly plan</p>
        <p>- Save $50 off</p>
        <div class="b-choose-this-plan">Choose this Plan</div>
      </div>
    </b-col>
  </b-row>
</template>

<script>
export default {
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
#main-choose-this-plan {
  align-content: center;
  display: flex;
}
</style>
