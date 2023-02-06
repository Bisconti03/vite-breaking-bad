<script >


export default {
  name: 'Card',
  props : {
    card: Object
  }
  
}

</script>

<template>

    <div>
        <div>
            <img :src="'https://images.ygoprodeck.com/images/cards/' + card.id + '.jpg'" class="w-100" alt="">
        </div>

        <div>
            <h4 class="text-light fs-5 py-3">
                {{card.name}}
            </h4>

            <h5 class="fw-normal">
                {{card.archetype}}
            </h5>
        </div>
    </div>
  

  
</template>

<style lang="scss" scoped>



</style>
