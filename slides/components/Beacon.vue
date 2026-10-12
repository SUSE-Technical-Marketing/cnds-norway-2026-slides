<script setup lang="ts">
// Beacon fires on the hilltops: the sagas describe warnings passed down the coast fire to fire.
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <path d="M2 58 Q16 36 30 36 Q44 36 50 58 Z" fill="#2A3A52" stroke="#8FB0CF" stroke-width="1.4" stroke-linejoin="round" />
    <path d="M38 58 Q48 46 56 46 Q62 48 63 58 Z" fill="#1F2D42" stroke="#8FB0CF" stroke-width="1.2" stroke-linejoin="round" />
    <path d="M20 36 L24 36 L26 32 L18 32 Z" fill="#8B5A2B" stroke="#3B2A1A" stroke-width="1" stroke-linejoin="round" />
    <path d="M22 32 Q12 24 20 14 Q20 20 24 20 Q22 12 26 6 Q34 16 30 24 Q30 20 28 20 Q32 28 22 32 Z" fill="#D0573F" stroke="#3B2A1A" stroke-width="1" stroke-linejoin="round" />
    <path d="M22 32 Q17 27 22 22 Q23 25 25 25 Q27 28 22 32 Z" fill="#E2A63D" />
    <path d="M54 46 Q50 42 54 38 Q55 41 57 41 Q59 44 54 46 Z" fill="#D0573F" stroke="#3B2A1A" stroke-width=".8" stroke-linejoin="round" />
    <path d="M10 14 L6 10 M34 12 L38 8 M8 24 L3 24" stroke="#E2A63D" stroke-width="1.4" stroke-linecap="round" />
  </svg>
</template>
