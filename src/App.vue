<template>
  <div id="app">
    <JsonToHtml />
  </div>
</template>

<script>
import JsonToHtml from "./components/json2html.vue";

export default {
  name: "App",
  components: {
    JsonToHtml,
  },
};
</script>
