<script setup>
import { useGlobalStore } from '@/stores/global';

const store = useGlobalStore()
</script>

<template>
  <header class="c-header">
    <div class="c-header__text">
      Le header
    </div>
    <div class="c-header__count" @click="store.increment()">
      {{ store.count }}
    </div>
  </header>
</template>

<style lang="scss">
.c-header {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  font-size: 24px;
}
</style>
