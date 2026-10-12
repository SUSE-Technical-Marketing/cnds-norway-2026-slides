<script setup lang="ts">
// Square sail in red and white stripes on a mast and yard: the engine of
// the open-seas leg. Pairs with the longship for "where we choose to go".
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <path d="M32 4 V60" stroke="#8B5A2B" stroke-width="3" stroke-linecap="round" />
    <path d="M8 12 H56" stroke="#8B5A2B" stroke-width="2.6" stroke-linecap="round" />
    <path d="M10 13 Q32 20 54 13 L50 46 Q32 52 14 46 Z" fill="#F3F0E8" stroke="#3B2A1A" stroke-width="1.2" stroke-linejoin="round" />
    <path d="M18 15.5 L16.5 47 Q20 48 23 48.4 L24 17 Z M33 17.5 L33 50 Q36 50 39 49.6 L40 17.6 Z M46 16 L44 48.6 Q47 47.8 50 46.6 L52 14.4 Z" fill="#D0573F" />
    <path d="M10 13 Q32 20 54 13 L50 46 Q32 52 14 46 Z" stroke="#3B2A1A" stroke-width="1.2" stroke-linejoin="round" />
    <path d="M32 60 L22 52 M32 60 L42 52" stroke="#8B5A2B" stroke-width="2" stroke-linecap="round" />
  </svg>
</template>
