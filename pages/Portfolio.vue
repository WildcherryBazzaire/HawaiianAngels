<template>
  <b-container>
    <b-row>
      <template v-for="(item, index) in portfolios">
        <Portfolio-Card :key="item.text" :content="item" :position="index" />
      </template>
    </b-row>
  </b-container>
</template>

<script>
import PortfolioCard from '@/components/ActualPortfolioCard'
export default {
  components: {
    'Portfolio-Card': PortfolioCard
  },
  data() {
    return {
      portfolios: [
        {
          image: require('@/static/images/Neural_Analytics.png'),
          name: 'Neural Analytics',
          text:
            '​Neural Analytics (NA) is developing a product that will allow physicians, first responders and even laypeople to accurately and quickly determine the severity of brain trauma in the field. Our device will simplify brain injury diagnosis, reduce healthcare costs and improve patient outcomes.'
        },
        {
          image: require('@/static/images/Kiana_Analytics.png'),
          name: 'Kiana Analytics',
          text: `Kiana Analytics is a secure cloud-based big data analytics and customer engagement solution designed to empower bricks and mortar retailers with the types of consumer analytics and micro-targeting capabilities that until now have been the exclusive privilege of online retailers.By capturing real-time analytics of consumer traffic patterns, retailers can learn more about their customers and measure the effectiveness of marketing campaigns and merchandising`
        },
        {
          image: require('@/static/images/Happy_Hour_Pal.png'),
          name: 'Happy Hour Pal',
          text: `Happy Hour Pal makes happy hour information easily accessible, and creates a channel for businesses to reach receptive customers. Happy Hour Pal charges businesses a recurring membership fee, and promotes a businesses' happy hour menu to an eager audience that is actively looking for happy hour information. `
        },
        {
          image: require('@/static/images/Selly_Automotive.png'),
          name: 'Selly Automotive',
          text:
            'Selly Automotive is a mobile first sales platform for dealerships and sales people. We offer the sales person a freemium app with all the core tools they need and the ability to buy leads on demand. For the dealership we provide an intuitive sales system with minimal training for a fraction of the cost of competitors. Dealerships spend over $4 billion a year on software and Selly is positioned to disrupt the industry.'
        },
        {
          image: require('@/static/images/Maclear.png'),
          name: 'Maclear',
          text:
            'Maclear’s enterprise, governance, risk and compliance (eGRC) suite is a unique next-generation software solution. It is a fast, easy, and powerful - yet affordable and scalable SaaS-based GRC automation solution that provides out-of-the-box functionality that can be implemented in weeks to provide a fully integrated system for all GRC requirements. Out-of-the-box modules include Vendor Risk Management, Asset Management, Risk Management, Threat Management, Business Continuity Management, Policy and Compliance Management, & Audit Management.'
        },
        {
          image: require('@/static/images/Findable_EXIT.png'),
          name: 'Findable',
          text:
            'Headquartered in Silicon Valley, California, Findables uses creative technology to make cool and practical products.  We pay close attention to details that others ignore, and feel passionate towards improving user experience. We love what we do, and find it boring to be like everyone else.'
        }
      ]
    }
  }
}
</script>
