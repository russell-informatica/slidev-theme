<script setup lang="ts">
import { computed } from 'vue'
import { useNav } from '@slidev/client'

const { slides, currentPage } = useNav()

const topic = computed(() => {
  for (let i = currentPage.value - 1; i >= 0; i--) {
    const t = slides.value[i]?.meta?.slide?.frontmatter?.topic
    if (t)
      return t as string
  }
  return ''
})
</script>

<template>
  <div v-if="topic" class="deck-topic">
    <span class="eyebrow">{{ topic }}</span>
  </div>
</template>

<style scoped>
.deck-topic {
  position: absolute;
  top: 2.5rem;
  left: 3.5rem;
  z-index: 5;
  pointer-events: none;
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 0.6em;
  color: var(--slidev-theme-primary);
  font-family: var(--slidev-code-font-family);
  font-size: 0.8rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
}

.eyebrow::before {
  content: '';
  width: 1.8em;
  height: 2px;
  border-radius: 2px;
  background: var(--slidev-theme-primary);
}
</style>
