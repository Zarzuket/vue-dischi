<template>
  <section>
        <Album :info="element" v-for="(element,index) in filteredDisks" :key="index"/>
  </section>
</template>

<script>
import axios from "axios"
import Album from './Album.vue'
export default {
    name: "Albums",
    props:["selectgenere"],
    components:{
        Album
    },
    data(){
        return{
            album:[],
        }
    },
    created() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then( (respond) =>{
         this.album = respond.data.response;
        } )
    },
    computed:{
        filteredDisks(){
            if(this.selectgenere === "" || this.selectgenere === "All"){
                return this.album;
            } else {
                return this.album.filter((elm) => elm.genre == this.selectgenere)
            }
        }
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