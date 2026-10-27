<script setup lang="ts">
// The longship before the planks: keel, stems and four ribs, one per timber
// on the keel slide (jurisdiction, control, portability, transparency).
withDefaults(defineProps<{ width?: number }>(), { width: 260 })
const ribs = [
  ['M82 123 Q76 106 72 90', '#E2A63D'],
  ['M114 125.6 Q111 108 110 90', '#D0573F'],
  ['M146 125.6 Q149 108 150 90', '#4FA3A0'],
  ['M178 123 Q184 106 188 90', '#5B8CC9'],
]
</script>

<template>
  <svg :width="width" :height="width * 0.62" viewBox="0 0 260 160" aria-hidden="true">
    <!-- ribs -->
    <path v-for="([d, c], i) in ribs" :key="i" :d="d" :stroke="c" stroke-width="5" fill="none" stroke-linecap="round" />
    <!-- keel with dragon prow (left) and curled stern (right) -->
    <path d="M30 112 Q130 140 230 112" fill="none" stroke="#8B5A2B" stroke-width="7" stroke-linecap="round" />
    <path d="M30 112 Q14 84 22 56 Q30 40 40 46 Q46 52 38 56 Q30 56 32 64" fill="none" stroke="#8B5A2B" stroke-width="5" stroke-linecap="round" />
    <path d="M40 46 l7 -3" stroke="#E2A63D" stroke-width="2" stroke-linecap="round" />
    <path d="M230 112 Q252 80 242 52 Q236 44 230 50" fill="none" stroke="#8B5A2B" stroke-width="5" stroke-linecap="round" />
    <!-- waves -->
    <path d="M6 146 q14 -9 28 0 t28 0 t28 0 t28 0 t28 0 t28 0 t28 0 t28 0 t28 0" fill="none" stroke="#4FA3A0" stroke-width="3" stroke-linecap="round" />
    <path d="M20 156 q14 -8 28 0 t28 0 t28 0 t28 0 t28 0 t28 0 t28 0 t28 0" fill="none" stroke="#4FA3A0" stroke-width="2" stroke-linecap="round" opacity=".5" />
  </svg>
</template>
