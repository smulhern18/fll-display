<template>
    <select v-model="selected" class="max-width">
        <option disabled value="">Please select one</option>
        <option v-for="color in props.colors">
            {{ color }}
        </option>
    </select>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const selected = ref()

const props = defineProps(['colors'])

</script>

<style scoped>
    .max-width {
        width: 6em;
    }
</style>