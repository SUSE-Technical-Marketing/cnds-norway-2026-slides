<script setup lang="ts">
// Voyage bar: the talk is one voyage. Each slide that starts a chapter sets
// `chapter: "IV · The charts"` in its frontmatter. The longship sails along
// the bottom as the deck advances, and the waypoints mark chapter starts.
// Set `voyage: false` in a slide's frontmatter to hide the bar there.
// Lives in global-top (drawn above the slide) because global-bottom is drawn
// underneath the slide, where the solid background hides it.
import { computed, unref } from 'vue'
import { injectLocal } from '@vueuse/core'
import { useNav } from '@slidev/client'
import { injectionSlidevContext } from '@slidev/client/constants.ts'
import Longship from './components/Longship.vue'

// In PDF/PNG export each page gets its own nav context, so prefer the
// injected one and fall back to the global nav in the live show.
const ctx = injectLocal(injectionSlidevContext, null as any)
const nav: any = ctx?.nav ?? useNav()
const v = (x: any) => unref(x)

const chapters = computed(() =>
  v(nav.slides)
    .filter((r: any) => r.meta?.slide?.frontmatter?.chapter)
    .map((r: any) => ({ no: r.no, label: String(r.meta.slide.frontmatter.chapter) })),
)

const total = computed(() => v(nav.total))
const currentSlideNo = computed(() => v(nav.currentSlideNo))

const at = (no: number) => (total.value > 1 ? ((no - 1) / (total.value - 1)) * 100 : 0)

const shipPos = computed(() => at(currentSlideNo.value))

const current = computed(() => {
  const passed = chapters.value.filter((c: any) => c.no <= currentSlideNo.value)
  return passed.length ? passed[passed.length - 1].label : ''
})

const hidden = computed(() => v(nav.currentFrontmatter)?.voyage === false)
const chapterOpener = computed(() =>
  String(v(nav.currentFrontmatter)?.class ?? '').split(/\s+/).includes('voyage-open'),
)
</script>

<template>
  <Longship v-if="chapterOpener" class="voyage-opener-ship" :width="132" />
  <div v-if="!hidden" class="voyage">
    <div class="voyage-chapter">{{ current }}</div>
    <div class="voyage-track">
      <svg class="voyage-sea" viewBox="0 0 400 10" preserveAspectRatio="none" aria-hidden="true">
        <path d="M0 6 q10 -5 20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0 t20 0" />
      </svg>
      <div
        v-for="c in chapters"
        :key="c.no"
        class="voyage-mark"
        :class="{ passed: c.no <= currentSlideNo }"
        :style="{ left: at(c.no) + '%' }"
      >
        <span>{{ c.label.split('·')[0].trim() }}</span>
      </div>
      <svg class="voyage-ship" :style="{ left: shipPos + '%' }" viewBox="0 0 44 22" aria-hidden="true">
        <path d="M3 13 Q12 19 22 19 Q33 19 41 11" />
        <path d="M3 13 Q1 9 3 6" />
        <path d="M41 11 Q43 7 41 4" />
        <path d="M22 19 V2" />
        <path class="sail" d="M15 3 H29 L28 12 Q22 13.5 16 12 Z" />
        <path class="stripe" d="M19 3 V12.6 M25 3 V12.6" />
        <circle class="sh a" cx="13" cy="15.5" r="1.8" />
        <circle class="sh b" cx="19" cy="16.6" r="1.8" />
        <circle class="sh a" cx="25" cy="16.6" r="1.8" />
        <circle class="sh b" cx="31" cy="15.5" r="1.8" />
      </svg>
    </div>
  </div>
</template>

<style scoped>
.voyage {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: 34px;
  display: flex;
  align-items: center;
  gap: 18px;
  padding: 0 28px 4px 28px;
  pointer-events: none;
  font-family: ui-monospace, SFMono-Regular, 'SF Mono', Menlo, Consolas, monospace;
}

.voyage-chapter {
  flex: none;
  width: 150px;
  font-size: 9px;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: #E2A63D;
  opacity: 0.85;
  white-space: nowrap;
}

.voyage-track {
  position: relative;
  flex: 1;
  height: 22px;
}

.voyage-sea {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 2px;
  width: 100%;
  height: 8px;
  fill: none;
  stroke: #4FA3A0;
  stroke-opacity: 0.6;
  stroke-width: 1;
}

.voyage-mark {
  position: absolute;
  bottom: 0;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.voyage-mark::after {
  content: '';
  width: 5px;
  height: 5px;
  border-radius: 50%;
  border: 1px solid #8FB0CF;
  background: #0C121B;
  margin-top: 1px;
}

.voyage-mark span {
  font-size: 7px;
  letter-spacing: 0.08em;
  color: #98A5B6;
  opacity: 0.7;
}

.voyage-mark.passed::after { border-color: #E2A63D; background: #E2A63D; }
.voyage-mark.passed span { color: #E2A63D; }

.voyage-ship {
  position: absolute;
  bottom: 3px;
  width: 38px;
  height: 19px;
  transform: translateX(-50%);
  transition: left 0.6s ease;
  fill: none;
  stroke: #C08A4E;
  stroke-width: 1.8;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.voyage-ship .sail { fill: #F3F0E8; stroke: none; }
.voyage-ship .stripe { stroke: #D0573F; stroke-width: 2.4; }
.voyage-ship .sh { stroke: none; }
.voyage-ship .sh.a { fill: #D0573F; }
.voyage-ship .sh.b { fill: #E2A63D; }
</style>
