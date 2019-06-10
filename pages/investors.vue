<template>
  <b-container class="main">
    <b-row>
      <b-col>
        <h1>
          <hr class="dash" />
          Membership Levels
          <hr class="dash" />
        </h1>
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
      <b-col>
        <h1>
          <hr class="dash" />
          Become A Member
          <hr class="dash" />
        </h1>
        <h2>1. Pick A Plan</h2>
        <p>Pay with Paypal or Credit Card</p>
        <Plan></Plan>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import levels from '@/components/investors/levels.vue'
import plan from '@/components/investors/plan.vue'
export default {
  components: {
    Levels: levels,
    Plan: plan
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
.box {
  border: 1px solid;
  border-radius: 30px;
  box-shadow: 3px 3px black;
  height: 200px;
  left: 25%;
  position: relative;
  width: 300px;
}
.dash {
  border-color: #56a3a6;
  display: inline-block;
  width: 100px;
}
.divider {
  border-left: thick solid #b70304;
}
h1 {
  color: #b70304;
}
#main {
  max-width: 100%;
}
</style>
