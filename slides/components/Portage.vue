<script setup lang="ts">
// Double-ended hull riding on log rollers: the same shape at bow and stern,
// so it could reverse course, and light enough to haul overland between rivers.
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <path d="M2 56 H62" stroke="#8FB0CF" stroke-width="1.6" stroke-linecap="round" />
    <path d="M10 60 H20 M30 60 H44 M52 60 H58" stroke="#8FB0CF" stroke-width="1.2" stroke-linecap="round" opacity=".6" />
    <path d="M3 21 Q6 18 9 22 Q12 31 20 33.5 Q32 36 44 33.5 Q52 31 55 22 Q58 18 61 21 Q60 36 50 42.5 Q32 47.5 14 42.5 Q4 36 3 21 Z" fill="#C08A4E" stroke="#3B2A1A" stroke-width="1.4" stroke-linejoin="round" />
    <path d="M7 29 Q14 40 28 43.5 M57 29 Q50 40 36 43.5" stroke="#3B2A1A" stroke-width="1" stroke-linecap="round" />
    <path d="M11 31 Q20 37.5 32 37.5 Q44 37.5 53 31" stroke="#E2C48F" stroke-width="1" stroke-linecap="round" opacity=".8" />
    <circle cx="19" cy="37" r="2.2" fill="#D0573F" stroke="#3B2A1A" stroke-width=".8" />
    <circle cx="26.5" cy="39" r="2.2" fill="#E2A63D" stroke="#3B2A1A" stroke-width=".8" />
    <circle cx="37.5" cy="39" r="2.2" fill="#D0573F" stroke="#3B2A1A" stroke-width=".8" />
    <circle cx="45" cy="37" r="2.2" fill="#E2A63D" stroke="#3B2A1A" stroke-width=".8" />
    <g fill="#8B5A2B" stroke="#3B2A1A" stroke-width="1.1">
      <circle cx="17" cy="50.5" r="5" /><circle cx="32" cy="51.5" r="4.6" /><circle cx="47" cy="50.5" r="5" />
    </g>
    <g stroke="#C08A4E" stroke-width="1" fill="none">
      <circle cx="17" cy="50.5" r="2.2" /><circle cx="32" cy="51.5" r="2" /><circle cx="47" cy="50.5" r="2.2" />
    </g>
  </svg>
</template>
