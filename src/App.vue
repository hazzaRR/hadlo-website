<template>
  <div class="bg-gray-100 flex flex-col min-h-screen font-mono relative  w-full h-screen z-0">
    <NavBar />
    <ShoppingBag v-if="showBag" />
    <router-view class="flex-grow"/>
    <Footer/>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'
import NavBar from './components/NavBar.vue'
import Footer from './components/Footer.vue'
import ShoppingBag from './components/ShoppingBag.vue'

export default {
  components: {NavBar, Footer, ShoppingBag},
  setup() {

    const showBag = ref(true)
    const toggleShowBag = () => {
      showBag.value = !showBag.value
    }
    
    
    return {showBag }

  }

}

</script>

<style>
</style>
