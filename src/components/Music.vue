<template>
   <section class="song-card">
            <img :src="info.poster" :alt="info.author">
            <h4>{{info.title}}</h4>
            <div class="autore">{{info.author}}</div>
            <div class="anno">{{info.year}} </div>
            <div class="genere">{{info.genre}}</div>
          
   </section>

</template>

<script>
export default {
    name:'Music',
    props: ['info'],
}
</script>

<style scoped lang="scss">
.autore {
    color:#6e7071;
    margin: 5px;
}
.anno {
    color:#6e7071;
    margin: 5px;
}
img {
    width: 80%;
}
h4 {
    padding: 10px;
}

</style>