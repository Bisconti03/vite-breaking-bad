<script >
import axios from 'axios';
import CardFound from './CardFound.vue'
import Card from './Card.vue'
import {store} from '../store';
import DropDown from './DropDown.vue';

export default {
  name: 'AppMain',

  data() {
    return {
      store
    }
  },


  components: {
    CardFound,
    Card,
    DropDown,
  },

  methods: {
      filterArchetype() {
        axios
      .get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=' + this.store.variableArchetype)
      .then((response) => {
      console.log(response.data.data.slice(0,200));
      this.store.cards  = response.data.data.slice(0,200);

    });
      }
  },


  created() {
    axios
    .get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
    .then((response) => {
      console.log(response.data.data.slice(0,200));
      this.store.cards  = response.data.data.slice(0,200);
    });
  }
}

</script>

<template>
    
  <main class="py-3">
    <DropDown @search="filterArchetype()"/>
    <div class="container bg-light">

        <CardFound :cardsList="store.cards.length" /> 

        <div class="row d-flex justify-content-center ">
            <div class="col-2 g-0 my-2 mx-3 text-center bg-primary" v-for="card in store.cards">
                <Card :card="card" />
            </div>

  
        </div>

    </div>
  </main>
</template>

<style lang="scss" scoped>


</style>
