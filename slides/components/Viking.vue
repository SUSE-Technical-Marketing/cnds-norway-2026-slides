<script setup lang="ts">
// Bearded Viking. variant="real": rounded Gjermundbu-style helmet with
// spectacle guard (the only near-complete Viking-age helmet ever found).
// variant="myth": the horned helmet from films and operas, which no Viking
// actually wore. The talk's opening uses exactly that contrast.
withDefaults(defineProps<{ size?: number; variant?: 'real' | 'myth'; beard?: string }>(), {
  size: 140,
  variant: 'real',
  beard: '#C8553D',
})
</script>

<template>
  <svg :width="size" :height="size * 1.15" viewBox="0 0 120 138" aria-hidden="true">
    <!-- horns (myth only) -->
    <template v-if="variant === 'myth'">
      <path d="M32 46 Q10 40 8 12 Q20 30 38 34 Z" fill="#F3F0E8" stroke="#3B2A1A" stroke-width="1.5" stroke-linejoin="round" />
      <path d="M88 46 Q110 40 112 12 Q100 30 82 34 Z" fill="#F3F0E8" stroke="#3B2A1A" stroke-width="1.5" stroke-linejoin="round" />
    </template>
    <!-- face -->
    <ellipse cx="60" cy="70" rx="25" ry="24" fill="#E8B98F" />
    <ellipse cx="34" cy="70" rx="4" ry="6" fill="#D9A47A" />
    <ellipse cx="86" cy="70" rx="4" ry="6" fill="#D9A47A" />
    <!-- beard with two braids -->
    <path d="M35 70 Q30 108 60 130 Q90 108 85 70 Q76 90 60 90 Q44 90 35 70 Z" :fill="beard" stroke="#3B2A1A" stroke-width="1.3" stroke-linejoin="round" />
    <path d="M52 112 Q50 122 52 134 M68 112 Q70 122 68 134" stroke="#3B2A1A" stroke-width="1.2" fill="none" opacity=".6" />
    <rect x="48.5" y="120" width="7" height="4" rx="1.5" fill="#E2A63D" />
    <rect x="64.5" y="120" width="7" height="4" rx="1.5" fill="#E2A63D" />
    <!-- mustache and nose -->
    <path d="M42 86 Q51 79 60 84 Q69 79 78 86 Q69 85 60 89 Q51 85 42 86 Z" :fill="beard" stroke="#3B2A1A" stroke-width="1.1" stroke-linejoin="round" />
    <path d="M60 68 Q57 78 60 80 Q63 80 62 78" fill="none" stroke="#B9835B" stroke-width="1.6" stroke-linecap="round" />
    <!-- eyes -->
    <circle cx="49" cy="66" r="2.4" fill="#1B2533" />
    <circle cx="71" cy="66" r="2.4" fill="#1B2533" />
    <path d="M43 59 l10 1 M67 60 l10 -1" stroke="#7A3A26" stroke-width="2.2" stroke-linecap="round" />
    <!-- helmet -->
    <path d="M32 56 Q32 18 60 16 Q88 18 88 56 Z" fill="#7D93AA" stroke="#3B2A1A" stroke-width="1.5" />
    <path d="M60 16 V56 M34 38 Q60 30 86 38" stroke="#5D7187" stroke-width="2" fill="none" />
    <rect x="31" y="50" width="58" height="7" rx="2" fill="#5D7187" stroke="#3B2A1A" stroke-width="1.2" />
    <circle v-for="x in [38, 48, 72, 82]" :key="x" :cx="x" cy="53.5" r="1.3" fill="#E6EEF5" />
    <!-- spectacle guard (real only) -->
    <template v-if="variant === 'real'">
      <path d="M38 57 Q38 72 49 72 Q57 72 58 62 L62 62 Q63 72 71 72 Q82 72 82 57" fill="none" stroke="#5D7187" stroke-width="3.2" stroke-linejoin="round" />
      <path d="M60 57 V74" stroke="#5D7187" stroke-width="3.6" stroke-linecap="round" />
    </template>
  </svg>
</template>
