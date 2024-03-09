<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue'
import MenuBar from './components/MenuBar.vue'

const value = ref(['apple', 'banana', 'cherry'])

</script>

<template>


  <header>
    <MenuBar />
    <div class="card p-fluid">
      <Chips v-model="value" />
    </div>
    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">


      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div> -->
  </header>

  <RouterView />
</template>

<style scoped></style>
