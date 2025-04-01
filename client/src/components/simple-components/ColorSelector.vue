<template>
    <div class="selector">
        <select v-model="selected">
            <option disabled value="">Please select one</option>
            <option v-for="color in props.colors">
                {{ color }}
            </option>
        </select>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const selected = ref()

const props = defineProps(['colors'])

</script>

<style scoped>
.selector {
    margin: 0.5em;
}
</style>