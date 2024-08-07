<script setup lang="ts">
defineProps<{ label: string }>()
</script>

<template>
  <button class="btn">
    <template v-if="label">
      {{ label }}
    </template>
    <template v-else>
      <slot> Button </slot>
    </template>
  </button>
</template>

<style scoped>
.btn {
  @apply py-2 px-4 rounded-md text-base font-medium bg-zinc-100 text-zinc-950;
}
</style>
