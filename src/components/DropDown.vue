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

      

      this.store.archetypes  = response.data;

      console.log(response.data)

    });
  }
}

</script>

<template>
  <div class="container">
    <div class="row">
        <div class="col bg-primary">

          

            <div  class="dropdown py-3">
              <select @change="$emit('search')" v-model="store.variableArchetype" class="form-select multiple w-25" aria-label="Default select example">
                <option  selected value="">Archetype</option >
                <option 
                
                v-for="archetype in store.archetypes" 
                :value="archetype.archetype_name"
                >{{archetype.archetype_name }}
                </option>
                 
              </select>

             
            </div>


          
            

        </div>

       

    </div>
  </div>
</template>

<style lang="scss" scoped>



</style>
