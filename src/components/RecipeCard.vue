<script setup lang="ts">
import TopImage from "@/components/TopImage.vue";
import RecipeTextContent from "@/components/RecipeTextContent.vue";

defineProps<{
  recipe: any;
}>();
</script>

<template>
  <div
    class="flex flex-col bg-white rounded-3xl md:p-10 w-full max-w-[46rem] font-outfit text-stone-900 md:gap-10"
  >
    <TopImage :src="recipe.src" :alt="recipe.alt" />
    <RecipeTextContent :recipe />
  </div>
</template>
