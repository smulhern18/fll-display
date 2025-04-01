<template>
  <div class="background-page">
    <Header> </Header>
    <div class="flex-row">
      <FieldSetNumberSelector class="pad" @changed-picked="(value) => {
        picked = value
      }" />
      <FieldSetColorSelector class="pad" :color_array=color_array :numFields=picked />
    </div>
  </div>
</template>

<script setup lang="ts">
import Header from "@/components/Header.vue"
import { ref } from "vue";
import FieldSetNumberSelector from "./components/FieldSetNumberSelector.vue";
import FieldSetColorSelector from "./components/FieldSetColorSelector.vue";

let picked = ref(8)

const color_array = ["red", "orange", "yellow", "green", "blue", "purple", "brown", "white"]

</script>

<style lang="scss" scoped>
@import "@/styles/base.scss";

.background-page {
  background-color: $offwhite;
  min-height: 100vh;
}

.flex-row {
  display: flex;
  flex-direction: row;
  height: 5em;
}

.pad {
  margin: 2em;
  height: 5em;
}
</style>
