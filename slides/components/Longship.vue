<script setup lang="ts">
// Colored longship: dragon prow, striped square sail, shields on the rail,
// oars and teal waves.
withDefaults(defineProps<{ width?: number }>(), { width: 260 })
const shields = [
  ['#D0573F', '#F3F0E8'], ['#E2A63D', '#2F5D8A'], ['#4FA3A0', '#F3F0E8'],
  ['#D0573F', '#E2A63D'], ['#2F5D8A', '#F3F0E8'], ['#E2A63D', '#D0573F'],
]
</script>

<template>
  <svg :width="width" :height="width * 0.62" viewBox="0 0 260 160" aria-hidden="true">
    <!-- mast and sail -->
    <path d="M130 22 V104" stroke="#8B5A2B" stroke-width="4" />
    <path d="M82 22 H178" stroke="#8B5A2B" stroke-width="3.5" stroke-linecap="round" />
    <clipPath id="ls-sail"><path d="M86 24 H174 L170 86 Q130 94 90 86 Z" /></clipPath>
    <g clip-path="url(#ls-sail)">
      <rect x="80" y="20" width="100" height="80" fill="#F3F0E8" />
      <rect v-for="i in 5" :key="i" :x="80 + (i - 1) * 22" y="20" width="11" height="80" fill="#D0573F" />
    </g>
    <path d="M86 24 H174 L170 86 Q130 94 90 86 Z" fill="none" stroke="#3B2A1A" stroke-width="1.5" />
    <!-- oars -->
    <path v-for="i in 6" :key="'o' + i" :d="`M${66 + i * 20} 112 l-10 26`" stroke="#C08A4E" stroke-width="2.2" stroke-linecap="round" />
    <!-- hull -->
    <path d="M26 96 Q60 126 130 126 Q200 126 236 92 L230 108 Q196 136 130 136 Q64 136 32 110 Z" fill="#8B5A2B" />
    <path d="M26 96 Q60 126 130 126 Q200 126 236 92" fill="none" stroke="#E2A63D" stroke-width="2.5" stroke-linecap="round" />
    <path d="M34 108 Q66 130 130 130 Q194 130 228 104" fill="none" stroke="#5E3B1C" stroke-width="1.5" />
    <!-- dragon prow (left) and curled stern (right) -->
    <path d="M26 96 Q12 72 22 52 Q30 40 40 46 Q46 52 38 56 Q30 56 32 64" fill="none" stroke="#8B5A2B" stroke-width="5" stroke-linecap="round" />
    <path d="M40 46 l7 -3 M34 50 l1 0" stroke="#E2A63D" stroke-width="2" stroke-linecap="round" />
    <path d="M236 92 Q252 70 242 52 Q236 44 230 50" fill="none" stroke="#8B5A2B" stroke-width="5" stroke-linecap="round" />
    <!-- shields on the rail -->
    <g v-for="(s, i) in shields" :key="'s' + i" :transform="`translate(${62 + i * 27} 104)`">
      <circle r="10" :fill="s[1]" />
      <path d="M0 0 V-10 A10 10 0 0 1 10 0 Z M0 0 V10 A10 10 0 0 1 -10 0 Z" :fill="s[0]" />
      <circle r="10" fill="none" stroke="#3B2A1A" stroke-width="1.6" />
      <circle r="2.6" fill="#B9C6D3" />
    </g>
    <!-- waves -->
    <path d="M6 146 q14 -9 28 0 t28 0 t28 0 t28 0 t28 0 t28 0 t28 0 t28 0 t28 0" fill="none" stroke="#4FA3A0" stroke-width="3" stroke-linecap="round" />
    <path d="M20 156 q14 -8 28 0 t28 0 t28 0 t28 0 t28 0 t28 0 t28 0 t28 0" fill="none" stroke="#4FA3A0" stroke-width="2" stroke-linecap="round" opacity=".5" />
  </svg>
</template>
