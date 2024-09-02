<script setup lang="ts">
defineProps<{
  preparations: {
    title: string;
    value: string;
  }[];
}>();
</script>

<template>
  <div class="bg-rose-50 rounded-lg p-6 flex flex-col gap-4">
    <h2 class="text-lg text-rose-800 font-semibold">Preparation time</h2>

    <ul class="flex flex-col gap-1 list-inside list-disc">
      <li v-for="item in preparations" class="text-rose-800 pl-2">
        <span class="text-stone-600">
          <span class="font-bold">
            {{ item.title }}
          </span>
          :
          {{ item.value }}
        </span>
      </li>
    </ul>
  </div>
</template>
