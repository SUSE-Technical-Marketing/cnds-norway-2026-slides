<script setup lang="ts">
// The Thing: free people meeting in a ring of stones around the law rock, law made in the open.
withDefaults(defineProps<{ size?: number }>(), { size: 64 })
</script>

<template>
  <svg :width="size" :height="size" viewBox="0 0 64 64" fill="none" aria-hidden="true">
    <ellipse cx="32" cy="50" rx="29" ry="9" fill="#2A3A52" stroke="#8FB0CF" stroke-width="1.2" />
    <g fill="#98A5B6" stroke="#3B2A1A" stroke-width="1" stroke-linejoin="round">
      <rect x="6" y="38" width="6" height="10" rx="2" /><rect x="16" y="34" width="6" height="10" rx="2" /><rect x="26" y="32" width="6" height="9" rx="2" /><rect x="36" y="34" width="6" height="10" rx="2" /><rect x="46" y="38" width="6" height="10" rx="2" /><rect x="53" y="42" width="5" height="8" rx="2" />
    </g>
    <g fill="#B9C6D3" stroke="#3B2A1A" stroke-width="1" stroke-linejoin="round">
      <rect x="4" y="49" width="7" height="10" rx="2" /><rect x="13" y="52" width="7" height="10" rx="2" /><rect x="44" y="52" width="7" height="10" rx="2" /><rect x="53" y="49" width="7" height="10" rx="2" />
    </g>
    <path d="M20 54 Q22 43 32 41 Q42 43 44 54 Q32 58 20 54 Z" fill="#8B7A66" stroke="#3B2A1A" stroke-width="1.2" stroke-linejoin="round" />
    <path d="M27 42 L28 30 Q32 28 36 30 L37 42 Q32 44 27 42 Z" fill="#E2A63D" stroke="#3B2A1A" stroke-width="1" stroke-linejoin="round" />
    <circle cx="32" cy="25.4" r="4.2" fill="#F3F0E8" stroke="#3B2A1A" stroke-width="1" />
    <path d="M37 32 L43 24" stroke="#E2A63D" stroke-width="2.4" stroke-linecap="round" />
  </svg>
</template>
