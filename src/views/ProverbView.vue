<script setup>
import { ref } from "vue";

const proverbs = ref([
  { id: 1, text: "Agorɔ bɛsɔ a, efiri anɔpa" },
  { id: 2, text: "Anomaa antu a, obua da" },
  { id: 3, text: "Obanyansofoo yebu no be, yennka no asem" },


]);

const chips = ref([
  "Default", "Twi", "Ewe", "Ga", "Fante"
]);




</script>

<template>
  <main>

    <v-card :loading="loading" class="mx-auto my-12" max-width="374">
      <template v-slot:loader="{ isActive }">
        <v-progress-linear :active="isActive" color="deep-purple" height="4" indeterminate></v-progress-linear>
      </template>

      <v-img height="250" src="https://cdn.vuetifyjs.com/images/cards/cooking.png" cover></v-img>

      <v-card-item>
        <v-card-title>Cafe Badilico</v-card-title>

        <v-card-subtitle>
          <span class="me-1">Local Favorite</span>

          <v-icon color="error" icon="mdi-fire-circle" size="small"></v-icon>
        </v-card-subtitle>
      </v-card-item>

      <v-card-text>
        <v-row align="center" class="mx-0">
          <v-rating :model-value="4.5" color="amber" density="compact" size="small" half-increments readonly></v-rating>

          <div class="text-grey ms-4">
            4.5 (413)
          </div>
        </v-row>

        <div class="my-4 text-subtitle-1">
          $ • Italian, Cafe
        </div>

        <div>Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.</div>
      </v-card-text>

      <v-divider class="mx-4 mb-1"></v-divider>

      <v-card-title>Translate</v-card-title>

      <div class="px-4">
        <v-chip-group v-model="selection">
          <v-chip v-for="chip in chips">{{ chip }}</v-chip>


        </v-chip-group>
      </div>

      <!-- <v-card-actions>
        <v-btn color="deep-purple-lighten-2" variant="text" @click="reserve">
          Reserve
        </v-btn>
      </v-card-actions> -->
    </v-card>



  </main>
</template>
