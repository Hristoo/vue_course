<template>
  <div id="app">
  
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <div class="row">
      
        <app-header></app-header>
        <!-- begin main content -->
        <transition name="fade" mode="out-in">
          <div class="container">
          <router-view />
          </div>
        </transition>
        <!-- end main content -->

        <AppFooter></AppFooter>
      
    </div>
  </div>
</template>

<script>

// Shared 
import AppHeader from './components/shared/AppHeader.vue';
import AppFooter from './components/shared/AppFooter.vue';


export default {
  name: 'app',
  data() {
    return {
      title: 'This is some title'
    }
  },
  components: {
    // AppHeader: AppHeader,
    AppHeader,
    AppFooter: AppFooter
  }
}
 
</script>

<style lang="scss" scoped>

 .row {

    margin-right: 0px;
    margin-left: 0px;
}
  
  .fade-enter-active, .fade-leave-active {
      transition: opacity .5s;
  }
  .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
      opacity: 0;
  }
</style>
