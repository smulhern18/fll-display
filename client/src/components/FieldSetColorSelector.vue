<template>
    <div class="highlight-blue-background flex-column radius margin">
          <div class="centered fixed-height fixed-top-margin"> Field Set Color Assignments</div>
            <div class="flex-row less-padding fixed-top-margin space-between">
              <div class="flex-column less-padding space-between">
                <ColorSelector :colors=props.color_array />
                <ColorSelector :colors=props.color_array v-if="props.picked > 2"/>
                <ColorSelector :colors=props.color_array v-if="props.picked > 4"/>
                <ColorSelector :colors=props.color_array v-if="props.picked > 6"/>
              </div>
              <div class="flex-column less-padding space-between">
                <ColorSelector :colors=props.color_array />
                <ColorSelector :colors=props.color_array v-if="props.picked > 2"/>
                <ColorSelector :colors=props.color_array v-if="props.picked > 4"/>
                <ColorSelector :colors=props.color_array v-if="props.picked > 6"/>
              </div>
            </div>
        </div>
</template>

<script setup lang="ts">
    import ColorSelector from './ColorSelector.vue';
    const props = defineProps(["color_array", "picked"])
</script>

<style lang="scss">
@import "@/styles/base.scss";

    .highlight-blue-background {
        background-color: $highlight-blue;
        border-color: $highlight-blue;
    }

    .space-between {
        justify-content: space-between;
    }

    .margin {
  margin: 1em;
}
</style>