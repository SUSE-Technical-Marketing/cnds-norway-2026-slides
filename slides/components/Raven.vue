<script setup lang="ts">
// Raven (Huginn and Muninn): scouts that fly out and report back. Dependency mapping, seeing what you run.
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <path d="M4 56 H44" stroke="#8B5A2B" stroke-width="3" stroke-linecap="round" />
    <path d="M52 17 Q44 10 36 18 Q32 24 26 27 Q14 30 8 43 L5 52 L14 47 L13 55 L22 48 Q36 50 42 38 Q46 30 44 25 Q50 24 60 23 Z" fill="#2A3A52" stroke="#B9C6D3" stroke-width="1.4" stroke-linejoin="round" />
    <path d="M22 30 Q12 36 9 49 M28 34 Q20 40 17 51" stroke="#B9C6D3" stroke-width="1" stroke-linecap="round" opacity=".7" />
    <path d="M60 23 L50 22 L52 17 Z" fill="#E2A63D" stroke="#3B2A1A" stroke-width=".8" stroke-linejoin="round" />
    <circle cx="44" cy="19" r="1.7" fill="#E2A63D" />
    <path d="M30 49 L28 56 M36 48 L36 56 M26 56 H31 M33 56 H38" stroke="#B9C6D3" stroke-width="1.4" stroke-linecap="round" />
  </svg>
</template>
