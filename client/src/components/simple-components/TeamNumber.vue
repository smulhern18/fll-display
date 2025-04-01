<template>
    <div class="teamNumber">
        Team {{ props.number }}
    </div>
</template>

<script setup lang="ts">
    const props = defineProps(['number', 'fieldColor'])
</script>

<style lang="css" scoped>
    .teamNumber {
        color: Black;
        font-size: large;
        margin: auto;
        height: fit-content;
        width: fit-content;
    }
</style>