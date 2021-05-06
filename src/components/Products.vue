<template>
   <section class="music-card">

   </section>
</template>

<script>
// axios chiamate 
import axios from 'axios';
export default {
    name:'Products',
    // collezione dei dati 
    data() {
        return {
            apiURL: 'https://flynn.boolean.careers/exercises/api/array/music',
            musicCard: [],
            loading: true,
        }
    },
    created() {
        this.getMusicCard();
    },
    methods: {
        getMusicCard() {
            // chiamata API accediamo alla proprietà
            axios.get(this.apiURL)
            .then(res => {
                //console.log( res.data);
                this.musicCard = res.data;
            })
            .catch(err => {
                console.log('ERRORE', err);
            });
        }
    }
}
</script>

<style scoped lang="scss">

.card {
    width: 950px;
    margin: 0 auto;
    background: lightsalmon;
    height: 200px;
    width: 800px ;
}

</style>