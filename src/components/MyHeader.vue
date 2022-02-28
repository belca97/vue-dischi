<template>
<header>

    <img src="https://i.kinja-img.com/gawker-media/image/upload/s--ypN6iH9q--/c_fill,fl_progressive,g_center,h_900,q_80,w_1600/zrarqnhmkoaihvzss5ek.jpg" alt="">

</header>
</template>

<script>
export default {
    name:'MyHeader'
}
</script>

<style scoped lang='scss'>

    @import '../assets/style/variabili.scss';


header{
     height: 5vh;
     width: 100%;
     color: white;
     background-color: $colorHeader;

     img{
         height: 5vh;
         width: 5vw;
     }
 }

</style>