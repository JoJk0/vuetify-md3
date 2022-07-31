<template>
    <v-btn class="md-tonal-button material-theme" rounded="pill" variant="tonal">
        <div class="container">
            <slot></slot>
        </div>
    </v-btn>
</template>

<script lang="ts" setup>
import '../tokens/baseline.css';
const props = defineProps({

});

// const emit = defineEmits({});


</script>

<style lang="scss" scoped>
.md-tonal-button {
    background-color: var(--md-sys-color-secondary-container);
    box-shadow: var(--md-sys-color-shadow);
    font-family: var(--md-sys-typescale-label-large-font);
    line-height: var(--md-sys-typescale-label-large-line-height);
    font-size: var(--md-sys-typescale-label-large-size);
    font-weight: var(--md-sys-typescale-label-large-weight);
    color: var(--md-sys-color-on-secondary-container);
    text-transform: none;
    letter-spacing: 0.0125rem;
    height: 40px;
    padding-left: 24px;
    padding-right: 24px;

    .container {
        display: flex;
        gap: 8px;
        color: inherit;
    }
}
</style>