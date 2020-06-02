<template>
  <div class="buttons-group">
    <select v-on:change="changeColor">
      <option>Select Color</option>
      <option :value="color" v-for="color in colorsList.colors" :key="color">{{color}}</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "Buttons",
  props: ["colorsList", "changeColor"]
};
</script>