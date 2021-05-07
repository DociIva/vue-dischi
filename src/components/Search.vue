<template>
   <form  class="form">
     <div class="content-search">
         <!--cosi ma con i dati dinamici passando dal filgio al papa-->
         <select name="all" id="all" v-model="selected">
            <option value=""> Please select</option>
             <option value="">A</option>

         </select>
     </div>

   </form>
</template>

<script>
export default {
    name:'Search',
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
.content-search {

}
</style>