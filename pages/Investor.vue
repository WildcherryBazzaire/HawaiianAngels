<template>
  <b-container>
    <b-row>
      <!--Where the membershup levels would go-->
    </b-row>
    <b-row>
      <!--Become a member stuff -->
      <Category-Header
        :content="'Become A Member'"
        :additional-content="'Pay with Paypal or Credit Card'"
      />
      <b-col sm="12" class="page-sub-headers text-sm-center">
        <!--This the plan subheader -->
        <h2>1. Pick A Plan</h2>
      </b-col>
      <b-col sm="12">
        <!--Plans will have their own interwoven row in this column -->
        <b-row>
          <b-col> </b-col>
        </b-row>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import CategoryHeader from '@/components/CategoryHeader'
export default {
  components: {
    'Category-Header': CategoryHeader
  }
}
</script>
