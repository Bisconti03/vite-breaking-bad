<script >
import axios from 'axios';
import {store} from '../store';

export default {
  name: 'DropDown',

  data() {
    return {
      store,
      
    }
  },




  created() {
    axios
    .get('https://db.ygoprodeck.com/api/v7/archetypes.php')
    .then((response) => {

      

      this.store.archetypes  = response.data.results;

      console.log(response)

    });
  }
}

</script>

<template>
  <div class="container">
    <div class="row">
        <div class="col bg-primary">
            <div  class="dropdown py-3">
              <select  class="form-select multiple w-25" aria-label="Default select example">
                <option selected>Archetype</option >
                <option value="1">One</option>
                <option value="2">Two</option>
                <option value="3">Three</option>
              </select>
            </div>

        </div>

       

    </div>
  </div>
</template>

<style lang="scss" scoped>



</style>
