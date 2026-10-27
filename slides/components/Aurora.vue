<script lang="ts">
// Unique filter ids, so several auroras can exist in the DOM at once (overview, print).
let nextId = 0
</script>

<script setup lang="ts">
// Northern lights: soft blurred ribbons that sway, flare and dim on their own cycles.
// Used behind the title and closing slides; the .aurora class (style.css) positions it.
// Each ribbon morphs between three wavy shapes (SMIL, so it needs no CSS support).
const id = `aurora-blur-${nextId++}`

interface Ribbon {
  color: string
  width: number // stroke width at rest
  opacity: number // opacity at rest
  dur: number // seconds per cycle
  begin: number // negative offset, so the ribbons don't move in step
  shapes: string[] // first is the resting shape; the rest are visited and then looped back
}

const ribbons: Ribbon[] = [
  {
    color: '#3FD7A0', width: 46, opacity: 0.55, dur: 16, begin: 0,
    shapes: ['M-40 130 Q220 30 440 110 T1020 50', 'M-40 105 Q280 80 400 70 T1020 85', 'M-40 155 Q160 40 500 135 T1020 35'],
  },
  {
    color: '#5B8CC9', width: 34, opacity: 0.5, dur: 20, begin: -7,
    shapes: ['M-40 185 Q260 80 520 160 T1030 100', 'M-40 160 Q200 130 560 120 T1030 140', 'M-40 205 Q320 60 480 185 T1030 85'],
  },
  {
    color: '#B07CD8', width: 18, opacity: 0.35, dur: 13, begin: -4,
    shapes: ['M180 80 Q420 10 720 80', 'M150 95 Q460 55 760 50', 'M210 60 Q380 -10 700 105'],
  },
]

const ease = (n: number) => Array(n).fill('.45 0 .55 1').join(';')
const times = (n: number) => Array.from({ length: n + 1 }, (_, i) => (i / n).toFixed(2)).join(';')
const loop = (r: Ribbon) => [...r.shapes, r.shapes[0]].join(';')
const pulse = (a: number, b: number) => `${a};${b};${a}`
</script>

<template>
  <svg class="aurora" viewBox="0 0 980 552" preserveAspectRatio="none" aria-hidden="true">
    <defs>
      <filter :id="id" x="-20%" y="-50%" width="140%" height="200%">
        <feGaussianBlur stdDeviation="16" />
      </filter>
    </defs>
    <g :filter="`url(#${id})`" fill="none" stroke-linecap="round">
      <path v-for="r in ribbons" :key="r.color" :d="r.shapes[0]" :stroke="r.color" :stroke-width="r.width" :opacity="r.opacity">
        <animate attributeName="d" :dur="`${r.dur}s`" :begin="`${r.begin}s`" repeatCount="indefinite"
          calcMode="spline" :keyTimes="times(r.shapes.length)" :keySplines="ease(r.shapes.length)" :values="loop(r)" />
        <animate attributeName="opacity" :dur="`${Math.floor(r.dur / 2) + 3}s`" :begin="`${r.begin}s`" repeatCount="indefinite"
          calcMode="spline" keyTimes="0;.5;1" :keySplines="ease(2)" :values="pulse(r.opacity, +(r.opacity * 0.65).toFixed(2))" />
        <animate attributeName="stroke-width" :dur="`${Math.floor(r.dur / 2) + 1}s`" :begin="`${r.begin}s`" repeatCount="indefinite"
          calcMode="spline" keyTimes="0;.5;1" :keySplines="ease(2)" :values="pulse(r.width, +(r.width * 1.4).toFixed(1))" />
      </path>
    </g>
  </svg>
</template>
