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
    size="large"
    color="grey-darken-4"
    variant="outlined"
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
  border: 1px solid rgba(147, 197, 253, 0.45) !important;
  border-radius: 8px !important;
  box-shadow: 0 8px 18px rgba(59, 130, 246, 0.08) !important;
  padding-top: 12px !important;
  padding-bottom: 12px !important;
  transition: transform 0.2s ease, box-shadow 0.2s ease, opacity 0.2s ease;
}

.link-button:hover {
  transform: translateY(-2px) scale(1.01);
  box-shadow: 0 12px 22px rgba(59, 130, 246, 0.14) !important;
}

.link-button:active {
  transform: translateY(0);
}
</style>
