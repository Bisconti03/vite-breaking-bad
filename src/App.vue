<script >
import AppHeader from './components/AppHeader.vue'
import DropDown from './components/DropDown.vue'
import AppMain from './components/AppMain.vue'

export default {
  name: 'App',

  components: {
    AppHeader,
    DropDown,
    AppMain
  }
}

</script>

<template>

  
  <AppHeader/>
  <div class="bg-primary">
    <DropDown/>

    <AppMain/>
    

  </div>
</template>

<style lang="scss">
@import './styles/main.scss';




</style>
