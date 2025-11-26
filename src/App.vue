<script setup>
import { RouterLink, RouterView } from 'vue-router'
import foodFest from '@/assets/cape food.jpg'
import TierList from './components/TierList.vue'
</script>

<template>
  <section>
    <img id="food" :src="foodFest"/>
   <h1>this is where my other content goes</h1>

    <div class="wrapper">
      

    </div>
  </section>
  
  <TierList />
  <RouterView />
</template>

<style scoped>
#food{
  margin-top: 2rem;
  object-fit: cover;
  height: 200px;
  width: 600px;
  overflow: hidden;
}
</style>
