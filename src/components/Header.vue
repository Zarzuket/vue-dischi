<template>
  <div>
      <header>
          <div class="container_logo">
              <img src="../assets/spotify-logo.png" alt="">
          </div>
              <select name="" id="" v-model="genere" @change="$emit('change' , genere )">
                  <option value="All">All</option>
                  <option value="Rock">Rock</option>
                  <option value="Pop">Pop</option>
                  <option value="Metal">Metal</option>
                  <option value="Jazz">Jazz</option>
              </select>
      </header>
  </div>
</template>

<script>
export default {
    name:"Header",
data(){
    return{
        genere:"",
    }
}
}

</script>

<style lang="scss" scoped>
@import "../style/variables";
header{
    background-color: $Header_Disk;
    height: 4.125rem;
    width: 100%;
}

.container_logo{
    height: 100%;
    
    img{
        height: 100%;
        padding: .625rem;
    }
}

header{
    display: flex;
    justify-content: space-between;
}
</style>>
