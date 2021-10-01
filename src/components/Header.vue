<template>
  <div>
      <header>
          <div class="container_logo">
              <img src="../assets/spotify-logo.png" alt="">
          </div>
      </header>
  </div>
</template>

<script>
export default {
    name:"Header"
}
</script>

<style lang="scss" scoped>
@import "../style/variables";
header{
    background-color: $Header_Disk;
    height: 3.125rem;
    width: 100%;
}

.container_logo{
    height: 100%;
    
    img{
        height: 100%;
        padding: .625rem;
    }
}

</style>>
