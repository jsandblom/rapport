<script setup lang="ts">
import { computed, ref } from 'vue';

const namn = ref('Namn');
const pnr = ref('PNR');
const GV = ref('GV');
const fvikt = ref('Fvikt');
const avikt = ref('Avikt');
const dgammal = computed(() => {});
const motsvGV = computed(() => {});
const viktprocent = computed(() =>
  Math.round((100 * (avikt.value - fvikt.value)) / fvikt.value)
);
</script>

<template>
  <p>
    <input v-model="namn" placeholder="Namn" />
    <input v-model="pnr" placeholder="Personnummer" />
    <input v-model="GV" placeholder="GV" />
    <input v-model="fvikt" placeholder="Fvikt" />
    <input v-model="avikt" placeholder="Avikt" />
  </p>

  <p>{{ dgammal }} motsv {{ motsvGV }} vikt: {{ viktprocent }}%</p>
</template>
