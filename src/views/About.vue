<template>
<div class="home">
<div class="d-flex justify-center mt-5 mb-5">
  <h1>Product Catalog</h1>
</div>
  <div class="container" id="app">
    <div class="row">
     <div v-for="product in products" class="col-md-12 col-18 my-2">
      <div class="card h-100">
        <v-card>
          <v-col cols="15">
          <img v-bind:src="product.pic" width="1032" height="400" class="img-responsive"><br/>
          <mdb-card-title class="title">{{product.title}}</mdb-card-title><br/>
          <mdb-card-text>{{product.subtitle}}</mdb-card-text><br/><br/>
          <mdb-card-text>{{product.description}}</mdb-card-text>
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
      products: [
        {
          id:1,
          title:"My Vodafone First Product",
          subtitle:"Buy it today",
          pic:"https://picsum.photos/id/0/600/400",
          description:"The description of the first product which is based on Lorem Ipsum. Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque nisi voluptatum maiores, repudiandae quas sed nam doloribus architecto pariatur sint quos quaerat rem dolore veniam aspernatur, rerum ducimus sunt impedit?"
        },
        {
          id:2,
          title:"My Vodafone Second Product",
          subtitle:"Don\'t miss it",
          pic:"https://picsum.photos/id/20/600/400",
          description:"The description of the second product which is based on CupCake Ipsum. Tart toffee fruitcake cookie I love. Powder jelly beans chocolate. Fruitcake icing fruitcake bonbon wafer cotton candy wafer. Cheesecake tootsie roll bonbon cake candy. Fruitcake macaroon sugar plum. Tootsie roll cookie I love sweet roll chocolate cake I love oat cake. Gingerbread jelly I love pudding cookie candy canes. Jelly sugar plum jelly beans brownie I love cookie pie I love. Sugar plum jelly beans marzipan. Liquorice lemon drops pudding oat cake marzipan I love I love."
        },
        {
          id:3,
          title:"My Vodafone Third Product",
          subtitle:"Last chance to get it",
          pic:"https://picsum.photos/id/367/600/400",
          description:"The description of the third product which is based on Cheese Ipsum. Dolcelatte red leicester boursin. Cheeseburger croque monsieur macaroni cheese brie bavarian bergkase cream cheese monterey jack pecorino. Port-salut croque monsieur melted cheese edam edam goat cream cheese port-salut. Mascarpone port-salut cottage cheese say cheese chalk and cheese fromage frais macaroni cheese pecorino. Blue castello squirty cheese paneer bavarian bergkase smelly cheese caerphilly cheesy grin lancashire. Bocconcini hard cheese cheese and biscuits bocconcini say cheese fromage frais rubber cheese cheeseburger. Cheese slices cream cheese cheese and wine cheesecake stilton manchego cheese slices when the cheese comes out everybody\'s happy. Cheesecake chalk and cheese feta."
        },
        {
          id:4,
          title:"My Vodafone Fourth Product",
          subtitle:"Now for sale",
          pic:"https://picsum.photos/id/504/600/400",
          description:"The description of the fourth product which is based on Hipsum. I\'m baby chicharrones selvage drinking vinegar lo-fi, hammock master cleanse jean shorts green juice tumblr live-edge mixtape photo booth microdosing cred pinterest. Umami affogato beard cray dreamcatcher kale chips you probably haven\'t heard of them knausgaard gastropub microdosing four loko. Roof party heirloom asymmetrical gluten-free hell of. Church-key you probably haven\'t heard of them subway tile chia affogato vice selfies street art tacos whatever hell of synth taxidermy mlkshk. Flannel poutine chillwave neutra. Cray roof party intelligentsia food truck palo santo cred single-origin coffee, seitan biodiesel whatever poutine activated charcoal keytar. Ugh activated charcoal craft beer, drinking vinegar tacos wayfarers jean shorts."
        },
        {
          id:5,
          title:"My Vodafone Fifth Product",
          subtitle:"As cheap as it gets",
          pic:"https://picsum.photos/id/119/600/400",
          description:"The description of the second product which is based on Office Ipsum. Pro-sumer software translating our vision of having a market leading platfrom or productize game plan. High touch client we need evergreen content nobody\'s fault it could have been managed better code put it on the parking lot and that ipo will be a game-changer or let me know if you need me to crack any skulls. Canatics exploratory investigation data masking strategic staircase, yet this vendor is incompetent or meeting assassin, so but what\'s the real problem we\'re trying to solve here? so wheelhouse deploy."
        },
        {
          id:6,
          title:"My Vodafone Sixth Product",
          subtitle:"Huge discounts",
          pic:"https://picsum.photos/id/160/600/400",
          description:"The description of the second product which is based on Sagan Ipsum. The carbon in our apple pies hearts of the stars the only home we\'ve ever known colonies culture the ash of stellar alchemy. A still more glorious dawn awaits hundreds of thousands great turbulent clouds with pretty stories for which there\'s little good evidence across the centuries cosmic ocean. With pretty stories for which there\'s little good evidence network of wormholes two ghostly white figures in coveralls and helmets are softly dancing extraordinary claims require extraordinary evidence take root and flourish permanence of the stars and billions upon billions upon billions upon billions upon billions upon billions upon billions."
        }
      ]                 
    }
  }
}
</script>