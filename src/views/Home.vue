<template>
  <div class="home">
    <h1 class="text-center mt-10">Product Catalog</h1>
      <v-container class="mt-10 mb-10">
        <v-row>
          <v-col cols="12" md="6" lg="4"
          v-for="(product, i) in parsedProducts" :key="i" >
          <v-card>
          <img v-bind:src="product.pic" width="344" height="200" class="img-responsive">
          <v-card-title class="title">{{product.title}}</v-card-title>
          <v-card-text>{{product.subtitle}}</v-card-text>  
          <template v-slot:action-button>
          <v-row justify="end"><v-btn color="red" text@click="$router.push('/about/${product.id}')">SHOW MORE
          </v-btn></v-row>
          </template>
          </v-card>
          </v-col>
        </v-row>
      </v-container>
   </div>
</template>

<script>
import { products } from '@/assets/exercise'

export default {
  name: 'Home',
  data: () => ({
    parsedProducts: JSON.parse(products.value).products,
  }),
  computed: {
    product() {
      return this.parsedProducts.filter(
        (product) => product.id == this.$router.params.id
      )[0]
    },
  },
}
</script>