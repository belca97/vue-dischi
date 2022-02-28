<template>
   
 <div class="box-img">
    <img :src="disco.poster" alt="">
    <h3>{{disco.title}}</h3>
    <p>{{disco.author}}</p>
    <p>{{disco.year}}</p>
 </div>
  
</template>

<script>
export default {
    name:'CardDischi',
    props:{
        "disco": Object        
    }
}
</script>

<style scoped lang='scss'>

        @import './src/assets/style/variabili.scss';

    .box-img{
        padding: 10px 15px;
        background-color: $colorBoxImg;
        text-align: center;
        width: calc(100% / 5 - 40px);
        height: 40vh;
    }
    .box-img img{
        width: 100%;
        min-height: 200px;
    }

    h3{
        color: white;
    }
    p{
        color: $colorParagraph;
    }
</style>