<template>
  <div id="cont">
    <Card
      title="Neural Analytics"
      description="Neural Analytics (NA) is developing a product that will allow physicians, first responders and even laypeople to accurately and quickly determine the severity of brain trauma in the field. Our device will simplify brain injury diagnosis, reduce healthcare costs and improve patient outcomes."
      logo="https://www.hawaiiangels.org/uploads/2/3/4/9/23499640/174235.png?319"
    />
    <Card
      title="Kiana Analytics"
      description="Kiana Analytics is a secure cloud-based big data analytics and customer engagement solution designed to empower bricks and mortar retailers with the types of consumer analytics and micro-targeting capabilities that until now have been the exclusive privilege of online retailers.By capturing real-time analytics of consumer traffic patterns, retailers can learn more about their customers and measure the effectiveness of marketing campaigns and merchandising"
      logo="https://www.hawaiiangels.org/uploads/2/3/4/9/23499640/3721383.png?314"
    />
    <Card
      title="Happy Hour Pal"
      description="Happy Hour Pal makes happy hour information easily accessible, and creates a channel for businesses to reach receptive customers. Happy Hour Pal charges businesses a recurring membership fee, and promotes a businesses' happy hour menu to an eager audience that is actively looking for happy hour information.
"
      logo="https://www.hawaiiangels.org/uploads/2/3/4/9/23499640/1593695.png"
    />
  </div>
</template>

<script>
import Card from '../components/PortfolioCard.vue'

export default {
  components: {
    Card
  }
}
</script>

<style>
#cont {
  display: flex;
  flex-flow: row wrap;
}
</style>
