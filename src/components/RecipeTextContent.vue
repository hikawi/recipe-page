<script setup lang="ts">
import RecipeOverview from "@/components/RecipeOverview.vue";

defineProps<{
  recipe: any;
}>();
</script>

<template>
  <div class="py-10 px-8 flex flex-col gap-8">
    <RecipeOverview :title="recipe.title" :description="recipe.description" />

    <div class="bg-rose-50 rounded-lg p-4 flex flex-col gap-1">
      <h2 class="text-lg text-rose-800 font-bold">Preparation time</h2>

      <ul class="flex flex-col gap-1 list-disc">
        <li><span class="font-bold">Total</span>: Approximately 10 minutes</li>
        <li><span class="font-bold">Preparation</span>: 5 minutes</li>
        <li><span class="font-bold">Cooking</span>: 5 minutes</li>
      </ul>
    </div>

    <h2>Ingredients</h2>

    <div>
      2-3 large eggs Salt, to taste Pepper, to taste 1 tablespoon of butter or oil Optional
      fillings: cheese, diced vegetables, cooked meats, herbs
    </div>

    <h2>Instructions</h2>

    <div>
      Beat the eggs: In a bowl, beat the eggs with a pinch of salt and pepper until they are well
      mixed. You can add a tablespoon of water or milk for a fluffier texture. Heat the pan: Place a
      non-stick frying pan over medium heat and add butter or oil. Cook the omelette: Once the
      butter is melted and bubbling, pour in the eggs. Tilt the pan to ensure the eggs evenly coat
      the surface. Add fillings (optional): When the eggs begin to set at the edges but are still
      slightly runny in the middle, sprinkle your chosen fillings over one half of the omelette.
      Fold and serve: As the omelette continues to cook, carefully lift one edge and fold it over
      the fillings. Let it cook for another minute, then slide it onto a plate. Enjoy: Serve hot,
      with additional salt and pepper if needed.
    </div>

    <h2>Nutrition</h2>

    <div>
      The table below shows nutritional values per serving without the additional fillings. Calories
      277kcal Carbs 0g Protein 20g Fat 22g
    </div>
  </div>
</template>
