<template>
  <v-btn class="md-text-button material-theme" rounded="pill" variant="text">
    <div class="container">
      <slot />
    </div>
  </v-btn>
</template>

<script lang="ts" setup>
const props = defineProps({

})

// const emit = defineEmits({});
</script>

<style lang="scss" scoped>
.md-text-button {
  background-color: transparent;
  font-family: var(--md-sys-typescale-label-large-font);
  line-height: var(--md-sys-typescale-label-large-line-height);
  font-size: var(--md-sys-typescale-label-large-size);
  font-weight: var(--md-sys-typescale-label-large-weight);
  color: var(--md-sys-color-primary);
  text-transform: none;
  letter-spacing: 0.0125rem;
  height: 40px;
  padding-left: 24px;
  padding-right: 24px;
  &[disabled] {
    opacity: 0.38;
  }

  .container {
    display: flex;
    gap: 8px;
    color: inherit;
  }
}
</style>
