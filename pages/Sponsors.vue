<template>
  <b-container>
    <b-row>
      <b-col sm="12" class="page-headers">
        <span class="lines"></span>
        <h1>Sponsors</h1>
        <span class="lines"></span>
      </b-col>
    </b-row>
    <b-row class="mt-5">
      <template v-for="(sponsors, index) in dummyData">
        <Sponsor-Card :key="sponsors.text" :index="index" :content="sponsors" />
      </template>
    </b-row>
  </b-container>
</template>

<script>
import SponsorCard from '@/components/SponsorCard'
export default {
  components: {
    'Sponsor-Card': SponsorCard
  },
  data() {
    return {
      dummyData: [
        {
          image: require('@/static/sponsors/HI_Growth.png'),
          text:
            'The HI Growth Initiative is a State equity investment program designed to catalyze the development of an innovation ecosystem that supports entrepreneurial high growth businesses and creates high wage jobs for our people.  The HI Growth Initiative currently provides $20 million of investment capital that will focus on the critical building blocks of an innovation ecosystem: entrepreneur development, research, commercialization and the mobilization of startup investment capital​',
          link: 'http://hsdc.hawaii.gov/hi-growth-initiative/'
        },
        {
          image: require('@/static/sponsors/First_Hawaii_Bank.png'),
          text: `
First Hawaiian BankFirst Hawaiian Bank is Hawaii's oldest and largest financial institution with $14.3 billion in total assets and over $10 billion in deposits. It was founded in 1858 by Charles Reed Bishop and today retains his values and integrity. The bank offers a full range of personal and business financial products, including a full complement of wealth management services such as estate planning, insurance and investments all delivered by a fully qualified trusted advisor. The bank is owned by BNP Paribas, a leading global financial services institution.`,
          link: 'http://www.fhb.com/'
        },
        {
          image: require('@/static/sponsors/First_Hawaii_Bank.png'),
          text: `
First Hawaiian Bankirst Hawaiian Bank is Hawaii's oldest and largest financial institution with $14.3 billion in total assets and over $10 billion in deposits. It was founded in 1858 by Charles Reed Bishop and today retains his values and integrity. The bank offers a full range of personal and business financial products, including a full complement of wealth management services such as estate planning, insurance and investments all delivered by a fully qualified trusted advisor. The bank is owned by BNP Paribas, a leading global financial services institution.`,
          link: 'http://www.fhb.com/'
        },
        {
          image: require('@/static/sponsors/First_Hawaii_Bank.png'),
          text: `
First Hawaiian BankFrst Hawaiian Bank is Hawaii's oldest and largest financial institution with $14.3 billion in total assets and over $10 billion in deposits. It was founded in 1858 by Charles Reed Bishop and today retains his values and integrity. The bank offers a full range of personal and business financial products, including a full complement of wealth management services such as estate planning, insurance and investments all delivered by a fully qualified trusted advisor. The bank is owned by BNP Paribas, a leading global financial services institution.`,
          link: 'http://www.fhb.com/'
        }
      ]
    }
  }
}
</script>

<style>
.page-headers {
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
}
.lines {
  margin: auto 1rem;
  width: 53px;
  padding-top: 5px;
  border-bottom: 0.25px solid #6cd4ff;
}
</style>
