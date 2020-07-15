<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
       Example of a product list webpage using VueJS components.
    </p>
    <h2>Shoe Products Available:</h2>
    <ul>
      <li v-for="product in products" :key="product">
        {{ product }}
      </li>      
    </ul>    
  </div>
</template>

<script>
export default {
  name: 'ProductsList',
  data: function () {
    return {
      products:[
        'Running Sneakers',
        'All-Terrain Sneakers',
        'Walking Sneakers',
        'Casual Sneakers'
      ]
  }
  },
  props: {
    msg: String,    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2 {
  margin: 40px 0 0;
}
ul {
  margin: 2%;
}
li {
  margin: 1%;
  list-style-type: square;
  list-style-position: inside;
  color: #000;
}
a {
  color: #000;
}
</style>
