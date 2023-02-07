<script>
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
  }
}

</script>

<template>
    
  <main class="py-3">
    <DropDown />
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
