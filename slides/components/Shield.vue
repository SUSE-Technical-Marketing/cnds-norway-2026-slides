<script setup lang="ts">
// Round Viking shield: painted quarters, iron rim, central boss.
withDefaults(defineProps<{ size?: number; a?: string; b?: string; label?: string }>(), {
  size: 64,
  a: '#D0573F',
  b: '#F3F0E8',
  label: '',
})
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" aria-hidden="true">
    <circle cx="32" cy="32" r="29" :fill="b" />
    <path d="M32 32 L32 3 A29 29 0 0 1 61 32 Z" :fill="a" />
    <path d="M32 32 L32 61 A29 29 0 0 1 3 32 Z" :fill="a" />
    <circle cx="32" cy="32" r="29" fill="none" stroke="#3B2A1A" stroke-width="3" />
    <circle cx="32" cy="32" r="29" fill="none" stroke="#B9C6D3" stroke-width="1" />
    <template v-if="label">
      <circle cx="32" cy="32" r="15" fill="#0C121B" stroke="#E2A63D" stroke-width="1.5" />
      <text x="32" y="37.5" text-anchor="middle" fill="#E2A63D" style="font: 600 14px Georgia, serif; letter-spacing: 0">{{ label }}</text>
    </template>
    <template v-else>
      <circle cx="32" cy="32" r="8" fill="#8FA3B8" stroke="#3B2A1A" stroke-width="1.5" />
      <circle cx="30" cy="30" r="2.5" fill="#E6EEF5" />
    </template>
  </svg>
</template>
