<template>
  <b-container class="main">
    <b-row>
      <b-col sm="12">
        <Category-Header :content="'Membership Levels'" />
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
      <b-col sm="12">
        <b-col sm="2" offset-sm="5">
          <b-button
            id="b-get-started"
            @click="
              setActive(true)
              changeClass()
            "
            >Get Started</b-button
          >
        </b-col>
      </b-col>
      <b-col>
        <div v-if="active === true" id="target">
          <Category-Header :content="'Become a Member'" />
          <b-row align-h="center">
            <h2 class="h-plan-options">1. Pick A Plan</h2>
          </b-row>
          <b-row align-h="center">Pay with Paypal or Credit Card</b-row>
          <Plan
            @changeDisplay="setActive($event)"
            @setActiveOneTime="activedOneTime($event)"
            @setActiveReoccuring="activedReoccuring($event)"
          ></Plan>
        </div>
        <b-row align-h="center">
          <div v-if="activeOneTime === true || activeReoccuring === true">
            <b-row align-h="center">
              <h2 class="h-plan-options">2. Choose A Membership</h2>
            </b-row>
            <Plan2
              :prop-one-time="activeOneTime"
              :prop-reoccuring="activeReoccuring"
            ></Plan2>
          </div>
        </b-row>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import levels from '@/components/investors/levels.vue'
import plan from '@/components/investors/plan.vue'
import plan2 from '@/components/investors/plan2.vue'
import CategoryHeader from '@/components/CategoryHeader'
export default {
  components: {
    Levels: levels,
    Plan: plan,
    Plan2: plan2,
    'Category-Header': CategoryHeader
  },
  data() {
    return {
      activeOneTime: false,
      activeReoccuring: false,
      active: false,
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
  },
  methods: {
    setActive: function(parm) {
      this.active = parm
    },
    activedOneTime: function(parm) {
      this.activeOneTime = parm
    },
    activedReoccuring: function(parm) {
      this.activeReoccuring = parm
    },
    changeClass: function() {
      const element = document.getElementById('target')
      element.classList.toggle = 'goUp'
    }
  }
}
</script>

<style>
#target {
  z-index: 7;
}
.goUp {
  animation-name: goUp;
  animation-duration: 2s;
  animation-fill-mode: forwards;
}
@keyframes goUp {
  0% {
    top: initial;
  }
  25% {
    top: 100%;
  }
}
#b-get-started {
  margin-top: 40%;
  background-color: #de8f11;
  position: relative;
  z-index: 6;
}
.box {
  border: 1px solid;
  border-radius: 30px;
  box-shadow: 3px 3px black;
  height: 200px;
  position: relative;
  width: 300px;
}
.center-content {
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
}
.dash {
  border-color: #56a3a6;
  display: inline-block;
  width: 100px;
}
.divider {
  border-left: 10px solid #b70304;
  border-radius: 10px;
}
.hidden {
  display: none;
}
h1 {
  color: #b70304;
}
.h-main {
  margin-top: 100px;
}
#main {
  max-width: 100%;
}
</style>
<style scoped>
div {
  overflow-y: hidden;
  overflow-x: hidden;
}
</style>
