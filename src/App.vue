<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue'
import MenuBar from './components/MenuBar.vue'

const value = ref(['apple', 'banana', 'cherry'])

</script>

<template>

  <v-container>
    <!-- <MenuBar /> -->


    <RouterView />
  </v-container>

</template>

<style scoped></style>
