<script setup lang="ts">
import RecipeCard from "./components/RecipeCard.vue";
import omelette from "@/assets/simple_omelette.json";
</script>

<template>
  <main class="flex items-center flex-col justify-center min-h-screen h-fit w-full bg-stone-100">
    <RecipeCard :recipe="omelette" />
  </main>
</template>
