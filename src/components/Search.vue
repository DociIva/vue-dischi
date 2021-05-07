<template>
   <form  class="form">
     <div class="content-search">
         <select name="all" id="all"></select>
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