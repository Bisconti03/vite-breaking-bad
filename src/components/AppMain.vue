<script >
import CardFound from './CardFound.vue'

export default {
  name: 'AppMain',
  components: {
    CardFound
  }
}

</script>

<template>
    
  <main class="py-3">
    <div class="container bg-light">

        <CardFound/>

        <div class="row d-flex justify-content-center ">
  <div class="col-2 g-0 my-2 mx-3 text-center bg-primary" v-for="i in 15">
    <div>
        <img src="https://via.placeholder.com/150x200 " class="w-100" alt="">
    </div>

    <div>
        <h3>
            Card Name
        </h3>

        <h5>
            Card Specie
        </h5>
    </div>
  </div>

  
</div>

    </div>
  </main>
</template>

<style lang="scss" scoped>


</style>
