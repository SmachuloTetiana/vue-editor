<template>
  <textarea v-model="editorText" placeholder="add multiple lines" rows="5" cols="50"></textarea>
</template>

<script>
export default {
  name: "TextEditor",
  data() {
    return {
      editorText: ""
    };
  }
};
</script>