<script setup lang="ts">
import RecipeOverview from "@/components/RecipeOverview.vue";
import RecipePreparation from "@/components/RecipePreparation.vue";
import RecipeIngredients from "@/components/RecipeIngredients.vue";
import RecipeInstructions from "@/components/RecipeInstructions.vue";
import RecipeNutrition from "@/components/RecipeNutrition.vue";

defineProps<{
  recipe: any;
}>();
</script>

<template>
  <div class="py-10 px-8 flex flex-col gap-8">
    <RecipeOverview :title="recipe.title" :description="recipe.description" />
    <RecipePreparation :preparations="recipe.preparations" />
    <RecipeIngredients :ingredients="recipe.ingredients" />
    <hr class="border-stone-150" />
    <RecipeInstructions :instructions="recipe.instructions" />
    <hr class="border-stone-150" />
    <RecipeNutrition :nutrition="recipe.nutrition" />
  </div>
</template>
