<script >

import {store} from './store';
import AppHeader from './components/AppHeader.vue';

import AppMain from './components/AppMain.vue';

export default {
  name: 'App',

  components: {
    AppHeader,
    
    AppMain,
  },

  data() {
    return {
      store
    }
  },

  
  
};

</script>

<template>

  
  <AppHeader/>
  <div  class="bg-primary  ">
    

    <AppMain  />
    

  </div>
</template>

<style lang="scss">
@import './styles/main.scss';



</style>
