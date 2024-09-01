<script setup lang="ts">
defineProps<{
  title: string;
  description: string;
}>();
</script>

<template>
  <div class="flex flex-col gap-6">
    <h1 class="text-[2.5rem] font-young-serif leading-none">{{ title }}</h1>
    <p class="text-stone-600">
      {{ description }}
    </p>
  </div>
</template>
