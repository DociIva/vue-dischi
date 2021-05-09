<template>
   <section class="container">
       <div>
           <Search />
       </div>
       <div class="music-card">
           <div v-for="(song, index) in musicCard" :key="index" 
            class="content-music">
            <Music :info="song" />
       </div>
       </div>
   </section>
</template>

<script>
// axios chiamate 
import axios from 'axios';
import Search from '@/components/Search.vue';
import Music from '@/components/Music.vue';
export default {
    name:'Products',
    components: {
        Music,
        Search,
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
        },
    }
}
</script>

<style scoped lang="scss">
.music-card {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}
.content-music {
    max-width: 200px;
    text-align: center;
    color: #fff;
    margin: 14px;
    background-color: #2e3a46;
    padding: 40px;
    cursor: pointer;
}

</style>