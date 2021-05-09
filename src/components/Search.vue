<template>
   <form  class="form">
     <label for="select"> Filter By Gender</label>
         <!--cosi ma con i dati dinamici passando dal filgio al papa-->
         <select @change="$emit('selectGener', select)" v-model="select">
            <option value="">All</option>
            <option v-for="(genere, index) in genereLista" :key="genere + index" > {{genere}}</option>

         </select>
     

   </form>
</template>

<script>
export default {
    name:'Search',

    data() {
        return {
            genereLista : ['Rock', 'Pop', 'Jazz', 'Metal',],
            select: 'All',
        }
    },
}
</script>

<style scoped lang="scss">
.form {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 30px;
}
select {
    width: 100px;
    height: 50px;
   padding: 10px;
}
//.content-search {}
</style>