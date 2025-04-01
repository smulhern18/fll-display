<template>
  <div class="offwhite-background full-height">
    <Header> </Header>
    <div class="flex-row padding">
      <FieldSetNumberSelector />
      <FieldSetColorSelector />
    </div>
  </div>
</template>

<script setup lang="ts">
import Header from "@/components/Header.vue"
import { ref } from "vue";
import FieldSetNumberSelector from "./components/FieldSetNumberSelector.vue";
import FieldSetColorSelector from "./components/FieldSetColorSelector.vue";

const picked = ref(2)

const color_array = ref(["red", "orange", "yellow", "green", "blue", "purple", "brown", "white"])

</script>

<style lang="scss" scoped>
@import "@/styles/base.scss";

.offwhite-background {
  background-color: $offwhite;
}

.silver-background {
  background-color: $silver;
  border-color: $silver;
}

.full-height {
  min-height: 100vh;
}

.flex-row {
  display: flex;
  flex-direction: row;
}

.flex-column {
  display: flex;
  flex-direction: column;
}

.padding {
  padding: 2em;
}

.less-padding {
  padding: 1em;
}

.radius {
  border-radius: 5%;
}

.centered {
  margin: auto;
}

.space-between {
  justify-content: space-between;
}

.margin {
  margin: 1em;
}

.fixed-top-margin {
  margin-top: 1em;
}
</style>
