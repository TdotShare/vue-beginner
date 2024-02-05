<script >
export default {
  data() {
    return {
      name: 'Pokemon !'
    }
  },
  methods: {
    greet(str) {
      alert(`Hello ${str}!`)
    }
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


  </div>



</template>

<style>


</style>
