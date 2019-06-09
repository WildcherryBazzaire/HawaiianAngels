<template>
  <b-row class="justify-content-center">
    <b-col>
      <h2>{{ content[0].planName }}</h2>
      <img :src="content[0].image" />
    </b-col>
    <div class="divider"></div>
    <b-col>
      <h2>{{ content[1].planName }}</h2>
      <img :src="content[1].image" />
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
.divider {
  border-left: thick solid #ff0000;
}
</style>
