<script setup lang="ts">
// Side rudder (styrbord): a Viking ship was steered by a broad oar on the
// right-hand side. "Starboard" literally means the steering board.
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <path d="M14 8 L46 56" stroke="#8B5A2B" stroke-width="4.5" stroke-linecap="round" />
    <path d="M14 8 L46 56" stroke="#C08A4E" stroke-width="1.4" stroke-linecap="round" stroke-dasharray="3 5" />
    <path d="M10 6 L22 4 L24 12 L16 14 Z" fill="#A87140" stroke="#3B2A1A" stroke-width="1" stroke-linejoin="round" />
    <path d="M40 40 L52 34 Q60 44 54 58 L46 60 Q42 52 40 40 Z" fill="#C08A4E" stroke="#3B2A1A" stroke-width="1.2" stroke-linejoin="round" />
    <path d="M45 44 Q50 50 49 57 M50 40 Q55 47 53 55" stroke="#3B2A1A" stroke-width="1" stroke-linecap="round" />
    <circle cx="33" cy="30" r="2.2" fill="#E2A63D" />
  </svg>
</template>
