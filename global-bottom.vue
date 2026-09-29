<script setup lang="ts">
import { useSlideContext } from '@slidev/client'

const { $nav, $slidev } = useSlideContext()
</script>

<template>
  <div class="deck-footer">
    <span class="deck-footer__name">{{ $slidev.configs.author }}</span>
    <span class="deck-footer__page">{{ $nav.currentPage }} / {{ $nav.total }}</span>
  </div>
</template>

<style scoped>
.deck-footer {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 5;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0.55rem 1.75rem;
  font-family: var(--slidev-code-font-family);
  font-size: 0.68rem;
  letter-spacing: 0.02em;
  color: var(--c-text-muted);
  pointer-events: none;
}
</style>
