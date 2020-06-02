<template>
  <div class="hello">
    <Buttons v-model="colorsList" :colorsList="colorsList" :changeColor="changeColor" />
    <TextEditor />

    <p :style="{color: `${colorsList.selectedColor}`}">Hello</p>
  </div>
</template>

<script>
import TextEditor from "./TextEditor";
import Buttons from "./Buttons";

export default {
  name: "HelloWorld",
  data() {
    return {
      colorsList: {
        selectedColor: "",
        colors: [
          "Blue",
          "Red",
          "Purple",
          "Yellow",
          "Pink",
          "Green",
          "Orange",
          "Lime",
          "Black",
          "Grey",
          "Brown"
        ]
      }
    };
  },
  methods: {
    changeColor(event) {
      this.colorsList.selectedColor = event.target.value;
      console.log("color>>", this.colorsList.selectedColor);
    }
  },
  components: {
    TextEditor,
    Buttons
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
</style>