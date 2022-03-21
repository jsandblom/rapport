<script setup lang="ts">

const atry = "cm/H_2O"

const andning = [{
  namn: "luft",
  parametrar: [{}}
},
{ namn: "LFNC",
  parametrar: [
    {
    namn: "flöde", enhet: "l/min", min: 0, max: 4
    }
  ]
},
{
  namn: "HFNC",
  parametrar: [
    {
      namn: "flöde", enhet: "l/min", min: 0, max:8
    },
    {
      namn: "o2", enhet: "%", min: 21, max:100
    }
  ]
},
{
  namn: "CPAP",
  parametrar: [
    {
      namn: "tryck", enhet: atry, min: 3, max: 10
    },
    {
      namn: "o2", enhet: "%", min: 21, max: 100
    }
  ]
},
{
  namn: "2PAP",
  parametrar: [
    {
      namn: "högre", enhet: atry, min: 6, max: 10
    },
    {
      namn: "lägre", enhet: atry, min: 3, max: 7
    },
    {
      namn: "frekvens", enhet: "x/min", min: 20, max: 40
    },
    { namn: "o2", enhet: "%", min: 21, max: 100
    }
  ]
},
{
  namn: "SIPPV",
  parametrar: [
    {
      namn: "PEEP", enhet: atry, min: 3, max: 10
    },
    {
      namn: "PIP", enhet: atry, min: 10, max: 30
    },
    {
      namn: "frekvens", enhet: "x/min", min: 20, max:60
    },
    {
      namn: "o2", enhet: "%", min: 21, max: 100
    },
    {
      namn: "T_i/T_e", enhet: "", min: 0.3, max: 3
    }
  ]
},
{
  namn: "VKTS", parametrar: [{

  }]
},
{
  namn: "TK", parametrar: [{}]
},
{
  namn: "HFO", parametrar: [{}]
}
]
const maskin = ["Leoni", "Servo-N", "Wilamed", "Sipap", "Trilogy", "ingen"]
</script>

<template>
  <select v-model="andning">
    <option v-for="a in andning">{{ a.namn }}</option>
  </select>
</template>
