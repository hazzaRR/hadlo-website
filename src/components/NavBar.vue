<template>

  <div class=" bg-gray-100 text-black-100 py-3.5 px-6 shadow md:flex justify-between items-center">
  <div class=" bg-gray-100 text-black-100 py-3.5 px-6 mx-2 md:flex justify-between items-center">
    <router-link to="/"><img src="../assets/stussy_logo.png" alt="hadlo_logo" class=" h-12 w-12"></router-link>
    <div class="mx-2 md:flex justify-between items-center">
      <p class="mx-2 cursor-pointer hover:text-red-700" @click="toggleSearchBar">Search</p>

      <div v-if="searchBar">
        <span>Search</span>
        <input type="text" class="bg-gray-100 shadow outline-none" v-if="searchBar">
        <button @click="toggleSearchBar">X</button>
      </div>
        
    </div>
  </div>
  <div class="mx-2">
      <router-link to="/collections" class="mx-2 hover:text-red-700">Collections</router-link>
      <router-link to="/about" class="mx-2 hover:text-red-700">About</router-link>
      <router-link to="/contact" class="mx-2 hover:text-red-700">Contact</router-link>
      <span class="mx-2 hover:text-red-700">Bag</span>
    </div>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {

  setup() {


    const searchBar = ref(false)
    const toggleSearchBar = () => {
      searchBar.value = !searchBar.value
    }

    const showBag = ref(false)
    const toggleShowBag = () => {
      showBag.value = !showBag.value
    }


    return {searchBar, toggleSearchBar}
    
  }

}
</script>

<style>

</style>