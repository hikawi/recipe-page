<script setup lang="ts">
import RecipeCard from "@/components/RecipeCard.vue";
import RecipeRandomizer from "@/components/RecipeRandomizer.vue";

import omelette from "@/assets/simple_omelette.json";
import noodles from "@/assets/simple_noodles.json";
import { computed, ref } from "vue";

const recipes = [omelette, noodles];
const recipe = ref(0);
const passedRecipe = computed(() => recipes[recipe.value]);

function changeRecipe() {
  recipe.value = (recipe.value + 1) % recipes.length;
  window.scrollTo({ top: 0, behavior: "smooth" });
}
</script>

<template>
  <main
    class="flex items-center flex-col justify-center min-h-screen h-fit w-full bg-stone-100 gap-4 md:py-4"
  >
    <RecipeCard :recipe="passedRecipe" />
    <RecipeRandomizer @swap-recipe="changeRecipe" />
  </main>
</template>
