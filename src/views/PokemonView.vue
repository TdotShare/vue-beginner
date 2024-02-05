<script >
import PokemonList from '../components/PokemonList.vue';
import axios from 'axios';


export default {
  components: {
    PokemonList
  },
  data() {
    return {
      name: 'Pokemon !',
      dataPokemon : []
    }
  },
  methods: {
    greet(str) {
      alert(`Hello ${str}!`)
    },
    getPokemonAll() {
      axios.get(`https://pokeapi.co/api/v2/pokemon?limit=10&offset=0`)
      .then(res => {
        this.dataPokemon = res.data.results
      })
      .catch(err => {
        console.error(err); 
      })
    }
  },
  mounted() {
    this.getPokemonAll()
  }
}
</script>

<template>
  <div>
    <h1>This is an {{ name }}</h1>


    <v-btn

    :block="true"
    color='success'
    @click="greet('Pokemon')"

    > Button </v-btn>

    <div style="margin-top: 2%;"></div>

    <hr />

    <PokemonList :dataPokemon="dataPokemon" ></PokemonList>


  </div>



</template>

<style>


</style>
