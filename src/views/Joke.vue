<template>
<div class="home">
  <div class="container" id="app">
    <div class="row" align="center">
     <div v-for="product in product" class="col-md-12 col-18 my-2">
      <img v-bind:src="product.icon"><br/>
      <h1>Joke of the day:</h1><br/>
      <p>{{product.value}}</p>
      </div>
   </div>

   <div class="container" align="center">
   <div class="col-md-4 col-6 my-1" align="center">
      <div class="card h-50">
        <v-card align="center"> 
          <v-col cols="15">
            <h3>Search for joke</h3><br/>  
          <input type="text" v-model="search" placeholder="Type something the se..." /><br /><br /><br />
          <v-row justify="end"><v-btn class="white--text" color="green" v-on:click="greet">MAKE ME LAUGH</v-btn></v-row>
          </v-col>
        </v-card>
      </div>
    </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      product: [
        {
          icon:"https://assets.chucknorris.host/img/avatar/chuck-norris.png",
          value:"Chuck Norris sustained a serious laceration during a sword demonstration. Instead of going to the ER, Chuck fixed his wound with a staple gun."
        }
      ]               
    }
  }
}
</script>