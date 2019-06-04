<template>
  <b-container>
    <b-row>
      <b-col>
        <h1 class="d-flex justify-content-center">___Membership Levels___</h1>
      </b-col>
      <div class="w-100"></div>
      <template v-for="x in header">
        <Levels :key="x" :header="x"></Levels>
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
      header: ['Individuals', 'Company', 'Guests']
    }
  }
}
</script>
