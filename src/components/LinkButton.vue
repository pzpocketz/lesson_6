<script setup lang="ts">
interface Props {
  label: string
  url: string
  icon?: string
}

const props = withDefaults(defineProps<Props>(), {
  icon: 'mdi-link',
})
</script>

<template>
  <v-btn
    :href="props.url"
    block
    rounded="pill"
    size="large"
    color="grey-darken-4"
    class="text-none link-button"
    target="_blank"
    rel="noreferrer noopener"
  >
    <v-icon :icon="props.icon" start />
    {{ props.label }}
  </v-btn>
</template>

<style scoped>
.link-button {
  transition: transform 0.2s ease, box-shadow 0.2s ease, opacity 0.2s ease;
}

.link-button:hover {
  transform: translateY(-2px) scale(1.01);
  box-shadow: 0 10px 20px rgba(17, 24, 39, 0.15) !important;
}

.link-button:active {
  transform: translateY(0);
}
</style>
