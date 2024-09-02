<script setup lang="ts">
defineProps<{
  ingredients: string[];
}>();
</script>

<template>
  <div class="flex flex-col gap-6">
    <h2 class="text-brown-800 font-young-serif text-[1.75rem] leading-none">Ingredients</h2>
    <ul class="list-inside list-disc flex flex-col gap-2">
      <li v-for="item in ingredients" class="pl-2 text-brown-800">
        <span class="text-stone-600">
          {{ item }}
        </span>
      </li>
    </ul>
  </div>
</template>
