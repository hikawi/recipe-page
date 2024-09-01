<script setup lang="ts">
defineProps<{
  src: string;
  alt: string;
}>();
</script>

<template>
  <img :src :alt class="rounded-none md:rounded-xl w-full mx-auto" />
</template>
