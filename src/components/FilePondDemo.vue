<template>
  <div id="app">
    <file-pond
      name="test"
      ref="pond"
      label-idle="Drop files here or <span class='filepond--label-action'>Browse</span>"
      allow-multiple="true"
      accepted-file-types="image/jpeg, image/png"
      v-bind:files="myFiles"
    />
  </div>
</template>

<script>
import vueFilePond from "vue-filepond";
import "filepond/dist/filepond.min.css";
// Create component
const FilePond = vueFilePond();
export default {
  name: "FilePondDemo",
  data: function () {
    return { myFiles: [] };
  },
  components: {
    FilePond,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
