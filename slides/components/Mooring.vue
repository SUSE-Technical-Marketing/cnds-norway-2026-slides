<script setup lang="ts">
// Wooden bollard with a rope coiled round it: a ship tied up at someone
// else's quay. You may own the hull, but the quay decides when it leaves.
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <path d="M4 52 H60" stroke="#8FB0CF" stroke-width="2" stroke-linecap="round" />
    <path d="M6 58 Q14 55 22 58 T38 58 T58 58" stroke="#5B8CC9" stroke-width="1.6" stroke-linecap="round" />
    <path d="M24 52 V22 Q24 16 32 16 Q40 16 40 22 V52 Z" fill="#8B5A2B" stroke="#3B2A1A" stroke-width="1.2" stroke-linejoin="round" />
    <path d="M22 26 Q32 32 42 26 M22 33 Q32 39 42 33 M22 40 Q32 46 42 40" stroke="#E2C48F" stroke-width="2.4" stroke-linecap="round" />
    <path d="M42 33 Q52 34 56 44 Q58 50 52 52" stroke="#E2C48F" stroke-width="2.4" stroke-linecap="round" />
  </svg>
</template>
