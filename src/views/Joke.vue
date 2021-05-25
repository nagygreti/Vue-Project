<template>
<div class="home">
  <div class="container" id="app">
    <div class="row" align="center">
      <div class="col-md-12 col-18 my-2">
      <h1>Joke of the day:</h1><br/>

      <ul v-if="posts && posts.length">
        <p><strong>{{post.value}}</strong></p>
      </ul>

      </div>
    </div>
  </div>

  <div class="container" align="center">
   <div class="col-md-4 col-6 my-1" align="center">
      <div class="card h-50">
        <v-card align="center"> 
          <v-col cols="15">
            <h3>Search for joke</h3><br/>  
          <input type="text" v-model="search" placeholder="Type something the se..." /><br /><br /><br />
          <v-row justify="end"><v-btn class="white--text" color="green">MAKE ME LAUGH</v-btn></v-row>
          </v-col>
        </v-card>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  data() {
    return {
      posts: []
    }
  },
  created() {
    axios.get(`https://api.chucknorris.io/jokes/random`)
    .then(response => {
      this.posts = response.value
    })
  }
}
</script>