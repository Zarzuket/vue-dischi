<template>
    <div class="card">
        <div class="container_img">
            <img :src="info.poster" alt="">
        </div>
        <div class="container_info">
            <h3 class="title">{{info.title}}</h3>
            <p>{{info.author}}</p>
            <p>{{info.year}}</p>
        </div>
        
    </div>
</template>

<script>
export default {
name: "Album",
props: ["info"],
}
</script>

<style lang="scss" scoped>
 @import "../style/variables.scss";
.card{
        height: 18.75rem;
        width: calc(100% / 5 - 1.35rem);
        background-color: #2E3A46;
        display: flex;
        flex-direction: column;
        text-align: center;
        .container_img{
            width: 100%;
            padding: 1.25rem;

        }
    }
.container_info{
    text-align: center;
    h3{
        color: white;
        font-size: 1.75rem;
    }
    p{
        color: grey;
        font-weight: bold;
    }
}

img{
    width: 100px;
    height: 100px;
    }

</style>