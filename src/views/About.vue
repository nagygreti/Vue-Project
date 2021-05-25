<template>
  <v-container clas="mt-10 mb-10">
    <v-row>
      <v-col>
        <product-card :product="product" :height="400">
          <div class="mt-5 mb-5">
            <img v-bind:src="product.pic" width="1032" height="400" class="img-responsive"><br/>
            <mdb-card-title class="title">{{product.title}}</mdb-card-title><br/>
            <mdb-card-text>{{product.subtitle}}</mdb-card-text><br/><br/>
            <mdb-card-text>{{product.description}}</mdb-card-text>
          </div>
        </product-card>
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