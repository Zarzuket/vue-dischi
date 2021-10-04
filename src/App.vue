<template>
  <div id="app">
    <Header @change="search_genere"/>
    <Albums :selectgenere="selectedGenere"/>
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Albums from './components/Albums.vue'
// import HelloWorld from './components/HelloWorld.vue'
export default {
  name: 'App',
  // props: ["xxx"],
  components: {
    Header,
    Albums
    // HelloWorld
  },
  data(){
    return{
      selectedGenere: "",
    }
  },
  methods: {
    search_genere(abba){
      this.selectedGenere = abba;
      console.log(this.selectedGenere);
    }
  },
}
</script>

<style lang="scss">
  @import "./style/common.scss"
</style>
