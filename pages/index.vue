<script setup>
const { client } = usePrismic()
const { data: home } = await useAsyncData('home', () => client.getSingle('homepage'))
console.log(home);
</script>

<template>
  <div class="p-index">
<!--    <h1>{{ home.data }}</h1>-->
<!-- me renvoie : [ { "type": "heading1", "text": "The fastest delivery in your city", "spans": [ { "start": 24, "end": 33, "type": "strong" } ] } ]
-->
    <Hero :title="home.data.hero_title" :text="home.data.hero_text" :buttons="home.data.hero_buttons" />
    <RecipeCard v-bind="{ title: 'Titre de la recette', description: 'une description' }" />
    Page d'accueil
  </div>
</template>

<style lang="scss">
.p-index {
}
</style>
