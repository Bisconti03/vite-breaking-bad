<script >
import axios from 'axios';
import {store} from './store';
import AppHeader from './components/AppHeader.vue';
import DropDown from './components/DropDown.vue';
import AppMain from './components/AppMain.vue';

export default {
  name: 'App',

  components: {
    AppHeader,
    DropDown,
    AppMain
  },

  data() {
    return {
      store
    }
  },

  created() {
    axios
    .get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
    .then((response) => {

      console.log(response.data.data.slice(0,20));

      this.store.cards  = response.data.data.slice(0,20);

    });
  }
  
};

</script>

<template>

  
  <AppHeader/>
  <div class="bg-primary vh-100 ">
    <DropDown />

    <AppMain  />
    

  </div>
</template>

<style lang="scss">
@import './styles/main.scss';



</style>
