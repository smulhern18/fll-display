<template>
  <div class="silver-background">
    <div class="centered"> How many field sets per side?</div>
    <div class="flex-column">
      <div>
        <input type="radio" id="two" value=2 v-model="picked" @change="onChange" />
        <label for="two">Two</label>
      </div>

      <div>
        <input type="radio" id="four" value=4 v-model="picked" @change="onChange" />
        <label for="four">Four</label>
      </div>

      <div>
        <input type="radio" id="six" value=6 v-model="picked" @change="onChange" />
        <label for="six">Six</label>
      </div>

      <div>
        <input type="radio" id="eight" value=8 v-model="picked" @change="onChange" />
        <label for="eight">Eight</label>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const picked = ref(2)

const emit = defineEmits<{
  changedPicked: [value: number],
}>()

function onChange() {
  emit("changedPicked", picked.value)
}

</script>

<style lang="scss">
@import "@/styles/base.scss";


.silver-background {
  background-color: $silver;
  border-color: $silver;
  border-radius: 5%;
  padding: 1em;
}

.centered {
  margin: auto;
}

.flex-column {
  justify-content: space-between;
  height: 100%;
}
</style>