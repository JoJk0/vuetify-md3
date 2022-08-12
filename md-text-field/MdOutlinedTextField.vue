<template>
  <VTextField class="md-outlined-text-field material-theme" v-bind="props" variant="outlined" />
</template>

<script lang="ts" setup>
const props = defineProps({
//   ...VTextField.props,
} as typeof VTextField['props'])

// const emit = defineEmits({});
</script>

<style lang="scss" scoped>
.md-outlined-text-field {
    height: 56px;
    border-radius: var(--md-sys-shape-corner-extra-small);
    border-width: 1px;
    border-color: var(--md-sys-color-outline);
    color: var(--md-sys-color-on-surface-variant);
}
</style>
