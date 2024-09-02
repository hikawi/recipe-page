<script setup lang="ts">
defineProps<{
  instructions: {
    title: string;
    value: string;
  }[];
}>();
</script>

<template>
  <div class="flex flex-col gap-6">
    <h2 class="text-brown-800 font-young-serif text-[1.75rem] leading-none">Instructions</h2>
    <ol class="list-outside list-decimal flex flex-col gap-2 pl-5">
      <li v-for="item in instructions" class="pl-2 text-brown-800 font-bold">
        <span class="text-stone-600">
          {{ item.title }}
        </span>
        <span class="font-normal text-stone-600">: {{ item.value }}</span>
      </li>
    </ol>
  </div>
</template>
