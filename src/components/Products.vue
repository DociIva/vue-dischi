<template>
   <section class="music-card">
       <div v-for="(song, index) in musicCard" :key="index" 
            class="content-music">
            <Music :info="song" />
            
       </div>

   </section>
</template>

<script>
// axios chiamate 
import axios from 'axios';
import Music from '@/components/Music.vue';
export default {
    name:'Products',
    components: {
        Music,
    },
    // collezione dei dati 
    data() {
        return {
            apiURL: 'https://flynn.boolean.careers/exercises/api/array/music',
            musicCard: [],
            seccess: false,
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
               // console.log( res.data.response);
               this.musicCard = res.data.response;
            })
            .catch(err => {
                console.log('ERRORE', err);
            });
        }
    }
}
</script>

<style scoped lang="scss">
.music-card {
    width: 100%;
    height: 500px;
}
.content-music {
    width: 150px;
    height: 150px;
    background: red;
}

</style>