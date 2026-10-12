<script setup lang="ts">
// Boathouse (naust): where a Norwegian keeps the ship he owns. Gable end, wide door, prow inside.
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <path d="M2 56 H62" stroke="#8FB0CF" stroke-width="1.6" stroke-linecap="round" />
    <path d="M6 60 Q14 57 22 60 T38 60 T58 60" stroke="#5B8CC9" stroke-width="1.4" stroke-linecap="round" />
    <path d="M9 56 V32 L32 9 L55 32 V56 Z" fill="#A87140" stroke="#3B2A1A" stroke-width="1.4" stroke-linejoin="round" />
    <path d="M9 32 L32 9 L55 32" stroke="#E2C48F" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round" />
    <path d="M32 9 L26 4 M32 9 L38 4" stroke="#3B2A1A" stroke-width="1.6" stroke-linecap="round" />
    <path d="M14 32 V56 M20 26 V56 M44 26 V56 M50 32 V56" stroke="#3B2A1A" stroke-width="1" opacity=".55" />
    <path d="M18 56 V38 Q18 30 32 30 Q46 30 46 38 V56 Z" fill="#0C121B" stroke="#3B2A1A" stroke-width="1.4" />
    <path d="M22 56 Q23 49 32 48 Q41 49 42 56 Z" fill="#8B5A2B" stroke="#3B2A1A" stroke-width="1" stroke-linejoin="round" />
    <path d="M22 52.5 Q32 55 42 52.5" stroke="#E2A63D" stroke-width="1.2" stroke-linecap="round" />
    <path d="M32 48 Q29 42 32 37" stroke="#C08A4E" stroke-width="3" stroke-linecap="round" />
    <path d="M32 37 Q33 33 37 34 Q38 36 35 37 Q34 38 33 38 Z" fill="#C08A4E" stroke="#3B2A1A" stroke-width=".8" stroke-linejoin="round" />
    <circle cx="35" cy="35" r=".9" fill="#E2A63D" />
  </svg>
</template>
