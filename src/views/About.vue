<template>
  <v-container clas="mt-10 mb-10">
    <v-row>
      <v-col>
          <div class="mt-5 mb-5">
            <img v-bind:src="product.pic" width="1032" height="400" class="img-responsive">
            <v-card-title class="title">{{product.title}}</v-card-title>
            <v-card-text>{{product.subtitle}}</v-card-text>
            <v-card-text>{{product.description}}</v-card-text>
          </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { products } from '@/assets/exercise'

export default{
  name: 'About',
  data: () => ({
    parsedProducts: JSON.parse(products.value).product,
  }),
  computed: {
    product() {
      return this.parsedProducts.filter(
        (product) => product.id == this.$route.params.id
      )[0]
    },
  },
}
</script>