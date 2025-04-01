<template>
    <div class="silver-background less-padding radius margin">
        <div class="centered fixed-height"> How many field sets per side?</div>
        <div class="flex-column padding">
          <div>
            <input type="radio" id="two" value=2 v-model="picked"/>
            <label for="two">Two</label>
          </div>
          <div>
            <input type="radio" id="four" value=4 v-model="picked"/>
            <label for="four">Four</label>
          </div>

          <div>
            <input type="radio" id="six" value=6 v-model="picked"/>
            <label for="six">Six</label>
          </div>

          <div>
            <input type="radio" id="eight" value=8 v-model="picked"/>
            <label for="eight">Eight</label>
          </div>
        </div>
      </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';


const picked = ref(2)

</script>

<style>
@import "@/styles/base.scss";

</style>