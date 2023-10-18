<script setup>
import { useGlobalStore } from '@/stores/global';

const store = useGlobalStore()
</script>

<template>
  <header class="c-header">
    <div class="c-header__text">
      <NuxtLink to="/">Le header</NuxtLink>
    </div>
    <div class="c-header__count" @click="store.increment()">
      {{ store.cart }}
    </div>
  </header>
</template>

<style lang="scss">
.c-header {
  position: fixed;
  padding: 20px;
  background-color: orange;
  top: 0;
  left: 0;
  right: 0;
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  font-size: 24px;
}
</style>
