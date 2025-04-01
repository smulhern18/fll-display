<template>
    <div class="blue-container">
        <div class="text"> Field Set Color Assignments</div>

        <div class="field-groups">
            <ColorSelector :colors=props.color_array />
            <ColorSelector :colors=props.color_array />
        </div>
        <div class="field-groups">
            <ColorSelector :colors=props.color_array v-if="props.numFields > 2" />
            <ColorSelector :colors=props.color_array v-if="props.numFields > 2" />
        </div>
        <div class="field-groups">
            <ColorSelector :colors=props.color_array v-if="props.numFields > 4" />
            <ColorSelector :colors=props.color_array v-if="props.numFields > 4" />
        </div>
        <div class="field-groups">
            <ColorSelector :colors=props.color_array v-if="props.numFields > 6" />
            <ColorSelector :colors=props.color_array v-if="props.numFields > 6" />
        </div>
    </div>
</template>

<script setup lang="ts">
import ColorSelector from './simple-components/ColorSelector.vue';
const props = defineProps(["color_array", "numFields"])
</script>

<style lang="scss" scoped>
@import "@/styles/base.scss";

.blue-container {
    background-color: $highlight-blue;
    border-color: $highlight-blue;
    border-radius: 5%;
    display: flex;
    flex-direction: column;
}

.text {
    margin: auto;
    padding: 1em;
}

.field-groups {
    display: flex;
    flex-direction: row;
}
</style>