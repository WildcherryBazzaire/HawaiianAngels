<template>
  <b-container fluid class="text-sm-center">
    <b-row>
      <b-col md="12">
        <Home-Banner />
      </b-col>
    </b-row>
    <b-row>
      <Category-Header :content="'The Header'" />
      <b-col sm="12" offset-md="1" md="4">
        <b-img
          src="https://www.hawaiiangels.org/uploads/2/3/4/9/23499640/9824627.jpg?425"
        ></b-img>
      </b-col>
      <b-col sm="12" md="6" class="asymmetry-text">
        <b-img id="Aline" :src="require('@/static/Aline.svg')"></b-img>
        <b-img
          id="AlineCurve"
          :src="require('@/static/AlineCurve.svg')"
        ></b-img>
        <p>
          Hawaii Angels provides a forum for members to review investment
          presentations and share opinions about these opportunities. This forum
          also allows for networking with professionals of various backgrounds,
          and exploring new opportunities in Hawaii. The Hawaii Angels process
          is proven and well-suited to Hawaii's start-up scene. Since its
          founding in February 2002, the member angels have invested more than
          $30 million in nearly 60 companies. Hawaii Angels was founded by
          Robert Robinson Ph.D., a former Harvard Business School professor and
          nationally recognized expert on angel investing. Through his
          leadership, the Hawaii Angels network has become highly successful and
          well recognized in the Honolulu business community and beyond. Hawaii
          Angels was co-founded by Chenoa Farnsworth who is the manager of the
          Hawaii Angels network.
        </p>
        <b-button size="sm" style="float:right;">Become a Member</b-button>
      </b-col>
    </b-row>
    <b-row>
      <Category-Header :content="'Portfolio'" />
      <b-col sm="12">
        <b-row>
          <template v-for="items in portfolioDemo">
            <b-col :key="items.text" sm="3">
              <Portfolio-Card :content="items" />
            </b-col>
          </template>
          <b-col sm="12">
            <h1 id="view_more" offset-md="6">View More</h1>
          </b-col>
        </b-row>
      </b-col>
      <b-col>
        <b-row>
          <Category-Header :content="'Management Team'" />
          <b-col offset-md="1" sm="12" md="3">
            <b-img :src="require('@/static/chenoa.jpg')"></b-img>
          </b-col>
          <b-col sm="12" md="8">
            <b-row>
              <b-col sm="12">
                <h1>Chenoa Farnsworth</h1>
              </b-col>
              <b-col sm="10">
                <p>
                  Chenoa Farnsworth was one of the founding members of Hawaii
                  Angels in 2002. Chenoa has more than 15 years experience in
                  business strategy and private equity investing. Farnsworth is
                  the managing director at Blue Startups, Hawaii’s only angel
                  capital investment network. In 2006, she co-founded Kolohala
                  Ventures, a Hawai’i-based venture capital firm that has
                  invested $50 million into Hawai’i-based technology start-ups.
                  <br />
                  <br />
                  Ms. Farnsworth has reviewed hundreds of business plans and
                  helped her start-up clients raise over $30 million in
                  financing. Ms. Farnsworth earned a BA in political science
                  from the University of California at Santa Cruz in 1992 and an
                  Executive MBA from the University of Hawaii in 2000.
                </p>
              </b-col>
            </b-row>
          </b-col>
          <b-col offset-md="1" sm="12" md="8">
            <b-row>
              <b-col sm="12">
                <h1>Chenoa Farnsworth</h1>
              </b-col>
              <b-col sm="10">
                <p>
                  Chenoa Farnsworth was one of the founding members of Hawaii
                  Angels in 2002. Chenoa has more than 15 years experience in
                  business strategy and private equity investing. Farnsworth is
                  the managing director at Blue Startups, Hawaii’s only angel
                  capital investment network. In 2006, she co-founded Kolohala
                  Ventures, a Hawai’i-based venture capital firm that has
                  invested $50 million into Hawai’i-based technology start-ups.
                  <br />
                  <br />
                  Ms. Farnsworth has reviewed hundreds of business plans and
                  helped her start-up clients raise over $30 million in
                  financing. Ms. Farnsworth earned a BA in political science
                  from the University of California at Santa Cruz in 1992 and an
                  Executive MBA from the University of Hawaii in 2000.
                </p>
              </b-col>
            </b-row>
          </b-col>
          <b-col pull-md="1" sm="12" md="3">
            <b-img :src="require('@/static/chenoa.jpg')"></b-img>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import HomeBanner from '@/components/HomeBanner.vue'
import PortfolioCard from '@/components/PortfolioCard.vue'
import CategoryHeader from '@/components/CategoryHeader.vue'
export default {
  components: {
    'Home-Banner': HomeBanner,
    'Portfolio-Card': PortfolioCard,
    'Category-Header': CategoryHeader
  },
  data() {
    return {
      /*
      should we add a search feature?
      all the information is in Portfolio.vue
      */
      portfolioDemo: [
        {
          image: require('@/static/images/Neural_Analytics.png'),
          name: 'Neural Analytics',
          text:
            'Neural Analytics (NA) is developing a product that will allow physicians, first responders and even...'
        },
        {
          image: require('@/static/images/Ibis_Networks.png'),
          name: 'Ibis Network',
          text:
            'Ibis Networks creates a secure mesh network using 128-bit AES encryption and patented Intelisocket™ technology...'
        },
        {
          image: require('@/static/images/Kiana_Analytics.png'),
          name: 'Kiana Analytics',
          text: 'iana Analytics is a secure cloud-based big data analytics...'
        },
        {
          image: require('@/static/images/Happy_Hour_Pal.png'),
          name: 'Happy Hour Pal',
          text:
            'Happy Hour Pal makes happy hour informaiton easily accessible... '
        },
        {
          image: require('@/static/images/Selly_Automotive.png'),
          name: 'Selly Automotive',
          text:
            'Selly Automotive is a mobile first sales platform for dealerships and sales people. '
        },
        {
          image: require('@/static/images/Maclear.png'),
          name: 'Maclear',
          text: 'Maclear’s enterprise, governance, risk and compliance (eGRC)'
        },
        {
          image: require('@/static/images/Findable_EXIT.png'),
          name: 'Findable',
          text:
            'Headquartered in Silicon Valley, California, Findables uses creative tech'
        },
        {
          image: require('@/static/images/Tealet.png'),
          name: 'Tealet',
          text:
            'Tealet is a direct-from-grower e-commerce marketplace that allows...'
        },
        {
          image: require('@/static/images/Contix.png'),
          name: 'Contix',
          text:
            'Contixs mission is to provide value to traders and invenstors...'
        },
        {
          image: require('@/static/images/Mile_High_Organics.png'),
          name: 'Mile High Organic',
          text:
            'Mile High Organics is Americas first certified organic online grocery store..'
        },
        {
          image: require('@/static/images/Volta.png'),
          name: 'Volta',
          text:
            'Volta Industries builds public, free-to-use electric vehicle charging networks...'
        },
        {
          image: require('@/static/images/Tetris_Online.png'),
          name: 'Tetris Online',
          text:
            'Tetris Online, Inc. is the exclusive online license of The Tetris Company...'
        }
      ]
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.start-headers {
  display: inline-block;
  position: relative;
}

.start-headers::before {
  content: '';
  display: block;
  left: -29%;
  top: 50%;
  position: absolute;
  margin: 0 auto;
  width: 53px;
  padding-top: 5px;
  border-bottom: 0.25px solid #6cd4ff;
}

.start-headers::after {
  content: '';
  display: block;
  right: -29%;
  top: 50%;
  position: absolute;
  margin: 0 auto;
  width: 53px;
  padding-top: 5px;
  border-bottom: 0.25px solid #6cd4ff;
}

.asymmetry-text {
  position: relative;
}

#Aline,
#AlineCurve {
  position: absolute;
  top: -7%;
}

#AlineCurve {
  right: 0%;
}
#view_more {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  text-align: center;
  margin-top: 5%;
  margin-bottom: 2%;
}
</style>
