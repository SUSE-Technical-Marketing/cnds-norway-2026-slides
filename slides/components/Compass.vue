<script setup lang="ts">
// Sun compass, in the spirit of the wooden bearing dial found at Uunartoq,
// Greenland: navigation by the sun, no instrument from anyone else.
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <circle cx="32" cy="32" r="27" fill="#C08A4E" stroke="#3B2A1A" stroke-width="1.4" />
    <circle cx="32" cy="32" r="21" stroke="#3B2A1A" stroke-width="1" />
    <path d="M32 11 V16 M32 48 V53 M11 32 H16 M48 32 H53 M17 17 l3.5 3.5 M43.5 43.5 L47 47 M47 17 l-3.5 3.5 M20.5 43.5 L17 47" stroke="#3B2A1A" stroke-width="1.6" stroke-linecap="round" />
    <path d="M32 32 L38 20 L32 8 L26 20 Z" fill="#D0573F" stroke="#3B2A1A" stroke-width="1" stroke-linejoin="round" />
    <path d="M32 32 L38 44 L32 56 L26 44 Z" fill="#F3F0E8" stroke="#3B2A1A" stroke-width="1" stroke-linejoin="round" />
    <circle cx="32" cy="32" r="2.6" fill="#E2A63D" stroke="#3B2A1A" stroke-width="1" />
  </svg>
</template>
