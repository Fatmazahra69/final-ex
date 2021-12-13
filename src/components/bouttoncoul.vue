<template>
 <h1 :style="{ color:couleur }">Produits dans mon panier</h1>
 <ul>
 <li v-for="item in cart" v-bind:key={item}>{{item}}</li>
 </ul>
 
 <button v-on:click="$emit('enlarge-text')">Agrandir texte</button>
 
 <button v-on:click="$emit('update-cart', cart)">Passer ma commande</button>

 <button v-on:click="changerCouleur" >changer la couleur du titre</button>
 <button v-on:click="couleur='pink'">changer coucou</button>
 
</template>
 
<script>
export default {
 name: 'HelloWorld',
 data(){
 return {
 cart: ['pain', 'fromage', 'fleurs', 'vin'],
couleur:'blue'
 }
 },
 methods: {
  changerCouleur() {
    this.couleur = 'pink';
  }
 },
 props: {
 msg: String
 }
}
</script>
 
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
 margin: 40px 0 0;
}
ul {
 padding: 0;
}
li {
 margin: 0 10px;
}
a {
 color: #42b983;
}
.button {
  background-color: black;
  padding: 1em;
  color: white;
  margin-right: 1em;
}
</style>