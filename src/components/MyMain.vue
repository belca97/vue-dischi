<template>
<main class="py-3 d-flex align-items-center">
    <div class="container">
        <div class="row row-cols-2 row-cols-sm-3 row-cols-lg-5">
            <CardDischi class="col my-3 mx-3" v-for="(disco, index) in listaDischi" :key="index" 
            :disco="disco"/>
        </div>
    </div>

</main>
</template>

<script>
// integro axios, ricordarsi di fare un npm install axios tramite terminale
  const axios = require('axios');
  import CardDischi from './partials/CardDischi.vue'

export default {

    name:'MyMain',
    data (){
        return{
            listaDischi:[]
        }
    },
    components:{
        CardDischi,
    },
    methods: {
        getDischi() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((response) => {
                this.listaDischi = response.data.response;
                console.log(response);
            })
            .catch(function (error) {
                // handle error
                console.log(error);
            })
            .then(function () {
                // always executed
            });
        }
    },
    created (){
        this.getDischi();
    }
}
</script>

<style scoped lang='scss'>
    @import '../assets/style/variabili.scss';  
main{
    height: 95vh;
    background-color: $colorMain;
}
</style>