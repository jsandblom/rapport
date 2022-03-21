<script setup lang="ts">
import PatientPlats from './PatientPlats.vue';
import PatientId from './PatientId.vue';
</script>

<template>
  <label>Plats <PatientPlats /></label>
  <PatientId />
  <!-- namn, pnr, GVd, GVnu, fvikt, vikt nu, procent upp eller ner, ålder -->
  <PatientSocialt />
  <!-- föräldranamn, syskon, problem -->
  <PatientProblem />
  <!-- andningsstörning, bili, kir, hjärt, annat, kryssrutor? -->
  <PatientAndning />
  <!-- maskin, inställningar -->
  <PatientNutrition />
  <!-- sort, mängd, intervall, vätska, räknevätska -->
  <PatientLäkemedel />
  <!-- för inotropi också uträknat per kg -->
  <PatientAktuellt />
</template>
