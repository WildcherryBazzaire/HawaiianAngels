<template>
  <b-container fluid class="px-0">
    <Entre-Banner content="Hawaii's top investors at your fingertips." />
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
    </b-row>
    <b-row>
      <Category-Header :content="'Presenations'" />
      <b-col sm="12" class="presentation-card">
        <b-row>
          <b-col sm="12" md="5" offset-md="1">
            <Presentation-Cards>
              <b-card-title class="h1">Our Criteria</b-card-title>
              <b-card-text>
                Hawaii Angels are looking for start-up companies with strong
                teams, proprietary technology, and large potential markets.
              </b-card-text>
              <b-card-text>
                Both Hawaii and mainland opportunities are reviewed.
              </b-card-text>
            </Presentation-Cards>
          </b-col>
          <b-col sm="12" md="5">
            <Presentation-Cards>
              <b-card-title class="h1">Screening Process</b-card-title>
              <b-card-text>
                Business plans submitted to Hawaii Angels will be reviewed by
                the Hawaii Angels Screening Committee. Two plans are chosen each
                month to present to the full group at the monthly Hawaii Angels
                meeting.
              </b-card-text>
            </Presentation-Cards>
          </b-col>
        </b-row>
        <b-row class="py-5">
          <b-col sm="12" md="4" offset-md="4">
            <Tip-Cards />
          </b-col>
        </b-row>
      </b-col>
    </b-row>
    <b-row align-h="center"> </b-row>
  </b-container>
</template>

<script>
import CategoryHeader from '@/components/CategoryHeader'
import EntrepreneurBanner from '@/components/EntrepreneurBanner'
import PresentationCards from '@/components/PresentationCards'
import TipCard from '@/components/TipCard'
export default {
  components: {
    'Category-Header': CategoryHeader,
    'Entre-Banner': EntrepreneurBanner,
    'Presentation-Cards': PresentationCards,
    'Tip-Cards': TipCard
  },
  data() {
    return {
      bannerImage: require('@/static/black_and_white.jpg')
    }
  }
}
</script>
