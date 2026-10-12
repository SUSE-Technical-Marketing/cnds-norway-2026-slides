<script setup lang="ts">
// Longhouse: long bowed walls under a turf roof, smoke hole, crossed gable beams. After Borg, Lofoten.
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <path d="M2 56 H62" stroke="#8FB0CF" stroke-width="1.2" stroke-linecap="round" opacity=".6" />
    <path d="M12 20 Q14 14 12 9 M18 18 Q20 12 17 6" stroke="#98A5B6" stroke-width="1.6" stroke-linecap="round" opacity=".7" />
    <path d="M7 38 Q10 25 32 23 Q54 25 57 38 L57 56 H7 Z" fill="#A87140" stroke="#3B2A1A" stroke-width="1.4" stroke-linejoin="round" />
    <path d="M3 40 Q8 20 32 17 Q56 20 61 40 Q50 31 32 31 Q14 31 3 40 Z" fill="#5E8A55" stroke="#3B2A1A" stroke-width="1.4" stroke-linejoin="round" />
    <path d="M11 26 Q22 21 32 21 Q42 21 53 26" stroke="#8DB27F" stroke-width="1.2" stroke-linecap="round" opacity=".7" />
    <path d="M9 17 L2 11 M9 17 L4 22 M55 17 L62 11 M55 17 L60 22" stroke="#C08A4E" stroke-width="1.8" stroke-linecap="round" opacity="0" />
    <path d="M14 38 V56 M22 36 V56 M30 35 V56 M38 35 V56 M46 36 V56 M52 38 V56" stroke="#3B2A1A" stroke-width="1" opacity=".5" />
    <path d="M26 56 V44 Q26 40 31 40 Q36 40 36 44 V56 Z" fill="#0C121B" stroke="#3B2A1A" stroke-width="1.2" />
    <rect x="42" y="42" width="5" height="4" fill="#E2A63D" stroke="#3B2A1A" stroke-width=".8" />
    <path d="M5 40 Q3 34 6 31 M59 40 Q61 34 58 31" stroke="#C08A4E" stroke-width="2.4" stroke-linecap="round" />
  </svg>
</template>
