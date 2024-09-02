<script setup lang="ts">
defineProps<{
  nutrition: {
    type: string;
    value: string;
  }[];
}>();
</script>

<template>
  <div class="flex flex-col gap-6">
    <h2 class="text-brown-800 font-young-serif text-[1.75rem] leading-none">Nutritions</h2>
    <p>The table below shows nutritional values per serving without the additional fillings.</p>

    <div class="flex-col flex gap-3">
      <template v-for="(item, index) in nutrition" :key="item.type">
        <div class="flex flex-row items-center justify-center text-left px-8 gap-4">
          <span class="text-left w-1/2">{{ item.type }}</span>
          <span class="font-bold text-left w-1/2 text-brown-800">{{ item.value }}</span>
        </div>
        <hr v-if="index !== nutrition.length - 1" class="border-stone-150" />
      </template>
    </div>
  </div>
</template>
