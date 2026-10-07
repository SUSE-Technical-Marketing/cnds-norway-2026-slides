<script setup lang="ts">
// Clinker-built hull: overlapping planks held by iron rivets. Every joint
// of a Viking ship was in plain sight, so anyone could see how it was made.
withDefaults(defineProps<{ width?: number }>(), { width: 40 })
</script>

<template>
  <svg :width="width" :height="width * 0.6" viewBox="0 0 40 24" aria-hidden="true">
    <path d="M2 3 Q20 7 38 3 L38 9 Q20 13 2 9 Z" fill="#C08A4E" stroke="#3B2A1A" stroke-width="1" />
    <path d="M2 8 Q20 12 38 8 L38 14 Q20 18 2 14 Z" fill="#A87140" stroke="#3B2A1A" stroke-width="1" />
    <path d="M2 13 Q20 17 38 13 L38 19 Q20 23 2 19 Z" fill="#8B5A2B" stroke="#3B2A1A" stroke-width="1" />
    <g fill="#E6EEF5">
      <circle cx="9" cy="9.6" r="1.1" /><circle cx="20" cy="11.2" r="1.1" /><circle cx="31" cy="9.6" r="1.1" />
      <circle cx="9" cy="14.6" r="1.1" /><circle cx="20" cy="16.2" r="1.1" /><circle cx="31" cy="14.6" r="1.1" />
    </g>
  </svg>
</template>
