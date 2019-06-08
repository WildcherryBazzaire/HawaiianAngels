<template>
  <b-col sm="12" class="mt-5">
    <b-row v-if="index % 2 === 0">
      <b-col sm="12" md="5">
        <b-img-lazy fluid center :src="content.image"></b-img-lazy>
      </b-col>
      <b-col offset-md="1" sm="12" md="6">
        <p>
          {{ content.text }}
        </p>
      </b-col>
    </b-row>
    <b-row v-else>
      <b-col sm="12" md="6">
        <p>
          {{ content.text }}
        </p>
      </b-col>
      <b-col offset="1" sm="12" md="5">
        <b-img-lazy fluid center :src="content.image"></b-img-lazy>
      </b-col>
    </b-row>
  </b-col>
</template>

<script>
export default {
  props: {
    content: Object,
    index: Number
  }
}
</script>
