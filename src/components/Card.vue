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
            <img :src="card.card_images.image_url" class="w-100" alt="">
        </div>

        <div>
            <h4 class="text-light ">
                {{card.name}}
            </h4>

            <h5>
                {{card.archetype}}
            </h5>
        </div>
    </div>
  

  
</template>

<style lang="scss" scoped>



</style>
