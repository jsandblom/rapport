<script setup lang="ts">
import { ref, computed } from 'vue';

const stad: 'Malmö' | 'Lund' = ref('Malmö');

const MalmöPlatser = [
  '5:1',
  '5:2',
  '5:3',
  '5:4',
  '5:5',
  '5:6',
  '5:X',
  '6:1',
  '6:2',
  '6:3',
  '6:4',
  '6:5',
  '6:6',
  '6:X',
  '7:1',
  '7:2',
  '7:3',
  '7:4',
  '7:5',
  '7:6',
  '7:X',
  'FV1:1',
  'FV1:2',
  'FV2:1',
  'FV2:2',
  'FV3:1',
  'FV3:2',
  'FV4:1',
  'FV4:2',
  '27:1',
  '27:2',
  '27:3',
];

const LundPlatser = [
  '1:1',
  '1:2',
  '1:3',
  '2:1',
  '2:2',
  '2:3',
  '3:1',
  '3:2',
  '4:1',
  '4:2',
  '4:X',
  '5:1',
  '5:2',
  '5:X',
  '6:1',
  '6:2',
  '7:1',
  '7:2',
  '8:1',
  '8:2',
  '10:1',
  '10:2',
  '10:3',
  '11:1',
  '11:2',
  '11:3',
  '12:1',
  '12:2',
  '12:3',
  '13:1',
  '13:2',
  '13:3',
  '14:1',
  '14:2',
  '14:3',
  '15:1',
  '15:2',
  '15:3',
];

const plats = computed(() =>
  stad.value == 'Malmö' ? MalmöPlatser : LundPlatser
);
</script>

<template>
  <label for="m"
    >Malmö<input type="radio" v-model="stad" id="m" value="Malmö"
  /></label>
  <label for="l"
    >Lund<input type="radio" v-model="stad" id="l" value="Lund"
  /></label>
  <select v-model="plats">
    <option v-for="p in plats">{{ p }}</option>
  </select>
</template>
