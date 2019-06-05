<template>
  <b-container class="main">
    <b-row>
      <b-col>
        <h1>---Membership Levels---</h1>
      </b-col>
      <template v-for="x in content">
        <Levels
          :key="x"
          :header="x.header"
          :text="x.text"
          :cost="x.cost"
          :image="x.image"
        ></Levels>
      </template>
    </b-row>
  </b-container>
</template>

<script>
import levels from '@/components/investors/levels.vue'
export default {
  components: {
    Levels: levels
  },
  data() {
    return {
      content: [
        {
          header: 'Indivduals',
          text:
            'Accredited investors that will be investing with their own capital.',
          cost: {
            headOne: 'In-State:',
            headTwo: 'Out-of-State',
            textOne: '$1,500',
            textTwo: '$750'
          },
          image: require('@/assets/investors/level_1.svg')
        },
        {
          header: 'Company',
          text:
            'Companies that are interested attending meetings (2 representatives) to support the organization mission or make direct investments.',
          cost: {
            headOne: 'Statewide:',
            headTwo: '',
            textOne: '$2,500',
            textTwo: ''
          },
          image: require('@/assets/investors/level_2.svg')
        },
        {
          header: 'Guests',
          text:
            'If you meet the above qualifications, you are welcome to attend a meeting as a guest before joining. Please contact info(at)hawaiiangels.org in advance to attend as a guest.',
          cost: {
            headOne: 'Meeting Costs:',
            headTwo: '',
            textOne: 'Free',
            textTwo: ''
          },
          image: require('@/assets/investors/level_3.svg')
        }
      ]
    }
  }
}
</script>

<style>
#main {
  max-width: 100%;
}
</style>
