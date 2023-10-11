<script setup>
const route = useRoute()
</script>

<template>
  <div class="p-recipe-id">
    recette avec l'id : {{ route.params.id }}
  </div>
</template>

<style lang="scss">

</style>
