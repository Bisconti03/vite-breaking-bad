<script >
import {store} from '../store';

export default {
  name: 'CardFound',
  // props: {
  //   cardsFound: {
  //     type: Number,
  //     default: 0
  //   }
  // },
  data() {
    return {
      store
    }
  },
}

</script>

<template>
  <div class="row pt-3">
    <div class="col mx-5 bg-black ">

        <p class="text-light pt-2 fw-bold">
            Found {{store.cards.length}} Cards
        </p>

    </div>

  </div>
</template>

<style lang="scss" scoped>



</style>
