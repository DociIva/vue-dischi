<template>
  <div id="app">
     <!--header-->
     <Header />

     <!--main / products / content-->
     <main>
       <Products />
     </main>


  </div>
</template>

<script>
// IMPORTARE IL COMPONENTE
import Header from '@/components/Header.vue';

import Products from '@/components/Products.vue';
export default {
  name: 'App',
  components: {
      Header,
      Products,
  }
}
</script>

<style lang="scss">
@import '@/styles/general';



</style>
