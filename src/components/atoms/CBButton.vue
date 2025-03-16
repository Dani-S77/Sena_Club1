<!-- src/components/atoms/CBButton.vue -->
<script setup lang="ts">
import { computed } from 'vue';

const variants = {
  blue: "bg-blue-500",
  red: "bg-red-500",
  cyan: "bg-cyan-500"
};

type ButtonProps = {
  variant?: 'blue' | 'red' | 'cyan',
  text: string
};

const props = withDefaults(defineProps<ButtonProps>(), {
  variant: 'blue'
});

const style = computed(() => variants[props.variant]);
</script>

<template>
  <button
    type="button"
    class="flex justify-center items-center rounded text-sm px-4 py-2"
    :class="style"
  >
    {{ text }}
  </button>
</template>
<style>
</style>