<script setup>
import { RouterView } from 'vue-router'
import Header from '@/components/Header.vue'
import NavBar from './components/NavBar.vue'
</script>

<template>
  <Header></Header>
  <NavBar></NavBar>
  <div class="screen-internal">
    <RouterView />
  </div>
</template>

<style scoped>
.screen-internal {
  margin-left: 250px;
  margin-top: 70px;
  height: 100vh;
}
</style>
