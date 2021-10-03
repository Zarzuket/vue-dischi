<template>
  <section>
      
    <!-- <div class="card">
        <img src="../assets/spotify-logo.png" alt="">
        <h3 class="title">deafa</h3>
        <p>erqwrq</p>
    </div> -->
    <!-- <div class="card">
    </div> -->
        <Album :info="element" v-for="(element,index) in album" :key="index"/>
  </section>
</template>

<script>
import axios from "axios"
import Album from './Album.vue'
export default {
    name: "Albums",
    components:{
        Album
    },
    data(){
        return{
            album:[]
        }
    },
    created() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then( (respond) =>{
         this.album = respond.data.response;
         console.log(this.album)
        } )
    }
}
</script>

<style lang="scss" scoped>

    section{
        max-width: 70rem;
        height: 45.25rem;
        margin: 5.125rem auto;
        display: flex;
        flex-wrap: wrap;
        padding: 20px;
        justify-content: space-evenly
    }

</style>>