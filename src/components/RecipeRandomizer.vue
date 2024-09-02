<script setup lang="ts">
defineEmits(["swapRecipe"]);
</script>

<template>
  <button
    class="bg-white rounded-lg fixed top-5 right-5 flex items-center justify-center px-4 py-2 hover:bg-brown-800 duration-150 hover:text-white"
    @click="$emit('swapRecipe')"
  >
    Swap recipe
  </button>
</template>
