<script setup lang="ts">
import { computed, reactive } from 'vue';

const problem = reactive({
  AS: false,
  bili: false,
  glu: false,
  kir: false,
  hjärt: false,
  utr: false,
  annat: false,
});
</script>

<template>
  <label><input type="checkbox" v-model="problem.AS" />AS</label>
  <label><input type="checkbox" v-model="problem.bili" />bili</label>
  <label><input type="checkbox" v-model="problem.glu" />glu</label>
  <label><input type="checkbox" v-model="problem.kir" />kir</label>
  <label><input type="checkbox" v-model="problem.hjärt" />hjärt</label>
  <label><input type="checkbox" v-model="problem.utr" />utr</label>
  <label><input type="checkbox" v-model="problem.annat" />annat</label>
</template>
