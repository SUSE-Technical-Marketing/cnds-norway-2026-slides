<script setup lang="ts">
// Bearded axe (skeggøx): the Viking woodworking and fighting axe.
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <path d="M18 60 L41 6" stroke="#8B5A2B" stroke-width="4.5" stroke-linecap="round" />
    <path d="M18 60 L41 6" stroke="#C08A4E" stroke-width="1.4" stroke-linecap="round" stroke-dasharray="3 5" />
    <path d="M35 12 L44 15 Q55 11 60 18 Q60 30 52 40 Q50 31 45 27 L39 24 Z" fill="#B9C6D3" stroke="#F3F0E8" stroke-width="1.4" stroke-linejoin="round" />
    <path d="M52 40 Q56 33 60 18" stroke="#F3F0E8" stroke-width="1.6" stroke-linecap="round" />
    <path d="M30 32 l6 2.5" stroke="#D0573F" stroke-width="2.5" stroke-linecap="round" />
  </svg>
</template>
