<script setup>

</script>

<template>
  <div class="p-index">
    <RecipeCard v-bind="{ title: 'Titre de la recette', description: 'une description' }" />
    Page d'accueil
    <div class="p-index__image">
      <NuxtImg src="/image-1.png" />
    </div>
  </div>
</template>

<style lang="scss">
.p-index {
}
</style>
