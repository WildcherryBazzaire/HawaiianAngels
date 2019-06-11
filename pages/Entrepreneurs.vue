<template>
  <b-container fluid class="px-0">
    <b-jumbotron fluid header="Hawaii's Top Investors at Your Fingertips">
    </b-jumbotron>
    <b-row>
      <Category-Header :content="'Application'" />
      <b-col sm="12" class="text-center">
        <p>
          Submit your application directly to our GUST system. Please attach an
          executive summary and full business plan to your application.
        </p>
      </b-col>
      <b-col sm="12" style="display: flex; justify-content: center;">
        <b-button>Apply Here</b-button>
      </b-col>
    </b-row>
    <b-row>
      <b-col
        sm="12"
        class="mt-5"
        style="display: flex; justify-content: center;"
      >
        <b-img :src="require('@/static/present.svg')" fluid></b-img>
      </b-col>
      <Category-Header :content="'Presenations'" />
    </b-row>
  </b-container>
</template>

<script>
import CategoryHeader from '@/components/CategoryHeader'
export default {
  components: {
    'Category-Header': CategoryHeader
  },
  data() {
    return {
      bannerImage: require('@/static/black_and_white.jpg')
    }
  }
}
</script>

<style scoped>
h1 {
  text-align: center;
  font-size: 48px;
  background: rgba(0, 0, 0, 0.3);
  border-radius: 1rem;
  padding: 5rem 0;
  color: #fcfcfc;
  font-weight: normal;
}

.jumbotron {
  background: url('https://www.hawaiiangels.org/uploads/2/3/4/9/23499640/2432007_orig.jpg');
  background-position: center;
  background-size: cover;
}
</style>
