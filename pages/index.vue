<template>
  <b-container fluid class="text-sm-center px-0">
    <b-row>
      <b-col md="12">
        <Home-Banner />
      </b-col>
    </b-row>
    <b-row>
      <Category-Header :content="'Who We Are'" />
      <b-col sm="12" offset-md="1" md="4">
        <b-img
          src="https://www.hawaiiangels.org/uploads/2/3/4/9/23499640/9824627.jpg?425"
          fluid
        ></b-img>
      </b-col>
      <b-col sm="12" md="6" class="asymmetry-text">
        <b-img id="Aline" :src="require('@/static/Aline.svg')"></b-img>
        <b-img
          id="AlineCurve"
          :src="require('@/static/AlineCurve.svg')"
        ></b-img>
        <p class="text-left" data-aos="fade-up">
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
      <Category-Header
        :content="'Portfolio'"
        :additional-content="'nearly 60 investments over 14 years'"
      />
      <b-col sm="12">
        <b-container>
          <b-row>
            <template v-for="(items, key) in portfolioDemo">
              <b-col v-if="key < 3" :key="items.text" class="px-0">
                <Portfolio-Card :content="items" />
              </b-col>
              <b-col v-else :key="items.text" class="px-0">
                <Portfolio-Card :content="items" />
              </b-col>
            </template>
            <b-col sm="12">
              <h1 id="view_more" offset-md="6">View More</h1>
            </b-col>
          </b-row>
        </b-container>
      </b-col>
      <b-col>
        <b-row>
          <Category-Header :content="'Management Team'" />
          <b-col offset-md="1" sm="12" md="3">
            <b-img
              :src="require('@/static/chenoa.jpg')"
              fluid
              class="manangement-image-1"
            ></b-img>
          </b-col>
          <b-col sm="12" md="8">
            <b-row>
              <b-col sm="12" class="pb-3 header-container">
                <b-img
                  :src="require('@/static/AlineBlue.svg')"
                  class="management-header-line"
                >
                </b-img>
                <h1 class="text-left management-name my-0">
                  Chenoa Farnsworth
                </h1>
                <h4 class="text-left management-role font-weight-light">
                  Managing Director
                </h4>
              </b-col>
              <b-col sm="10">
                <p class="text-left">
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
          <b-col offset-md="1" sm="12" md="7">
            <b-row>
              <b-col class="px-5 pb-3 header-container" sm="12">
                <b-img
                  :src="require('@/static/AlineBlue.svg')"
                  class="management-header-line"
                >
                </b-img>
                <h1 class="text-left management-name my-0">
                  Robert J. Robinson
                </h1>
                <h4 class="text-left management-role font-weight-light">
                  President
                </h4>
              </b-col>
              <b-col sm="10">
                <p class="text-left">
                  Hawaii Angels was founded as UH Angels by Robert J. Robinson,
                  Ph.D. Dr. Robinson is the Barry and Virginia Weinman
                  Distinguished Professor of Entrepreneurship and E-Business at
                  the University of Hawai`i, Shidler College of Business. He was
                  previously on the faculty of the Harvard Graduate School of
                  Business Administration.
                  <br />
                  <br />
                  Robert J. Robinson, Ph.D. is a nationally recognized expert on
                  angel investing, co-author of Angel Investing: Matching
                  Startup Funds with Startup Companies. He is also an
                  award-winning author on business negotiation and conflict
                  management, and has over 20 years of experience in coaching
                  companies in valuation and other negotiations.
                </p>
              </b-col>
            </b-row>
          </b-col>
          <b-col pull-md="1" sm="12" md="3">
            <b-img
              :src="require('@/static/robert.jpg')"
              fluid
              class="manangement-image-2"
            ></b-img>
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
        }
      ]
    }
  }
}
</script>

<style scoped>
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

.manangement-image-1,
.manangement-image-2 {
  border-radius: 0.625rem;
  margin: auto;
}

p,
h1,
h4 {
  color: #4f4e4c;
}

.manangement-image-1 {
  box-shadow: -16px 14px 0px rgba(219, 76, 64, 0.6);
}

.manangement-image-2 {
  box-shadow: 16px 14px 0px rgba(219, 76, 64, 0.6);
}

.header-container {
  position: relative;
}

.management-header-line {
  position: absolute;
  bottom: 14%;
  left: 6%;
}
</style>
