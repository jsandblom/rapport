<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import { reactive } from 'vue';
import Patient from './components/Patient.vue';

const patienter = reactive([]);

const nyPatient = function () {};
</script>

<template>
  <div v-if="patienter" v-for="p in patienter">
    <div>{{ p.plats }}</div>
    <div>{{ p.pnr }}</div>
    <div>{{ p.namn }}</div>
  </div>
  <Patient />
  <hr />
  <button @click="nyPatient">lägg till patient</button>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
