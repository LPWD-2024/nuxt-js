<script setup>
const { params } = useRoute()
const env = useRuntimeConfig()
const { data: recipe } = await useAsyncData(`recipe-${params.id}`, () => {
  return $fetch(`${env.public.apiUrl}/recipes/${params.id}`)
})
</script>

<template>
  <div class="p-recipe-id">
    recette avec l'id : {{ params.id }}
    <p>{{ recipe.recipe_name }}</p>
  </div>
</template>

<style lang="scss">

</style>
