<template>
    <v-btn class="md-filled-button material-theme" rounded="pill" variant="flat">
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
.md-filled-button {
    background-color: var(--md-sys-color-primary);
    font-family: var(--md-sys-typescale-label-large-font);
    line-height: var(--md-sys-typescale-label-large-line-height);
    font-size: var(--md-sys-typescale-label-large-size);
    font-weight: var(--md-sys-typescale-label-large-weight);
    color: var(--md-sys-color-on-primary);
    text-transform: none;
    letter-spacing: 0.0125rem;
    height: 40px !important;
    padding-left: 24px;
    padding-right: 24px;

    .container {
        display: flex;
        gap: 8px;
        color: inherit;
    }
}
</style>