<template>
  <div id="app">
    <toolbar />
    <multiselect v-model="value" :options="options"></multiselect>
    <note-container />
  </div>
</template>

<script>
import Multiselect from "vue-multiselect";
import Toolbar from "./components/Toolbar.vue";
import NoteContainer from "./components/NoteContainer.vue";
export default {
  name: "app",
  components: {
    Toolbar,
    NoteContainer,
    components: { Multiselect },
  },
  data() {
    return {
      value: null,
      options: ["list", "of", "options"],
    };
  },
};
//
</script>

<style>
src="vue-multiselect/dist/vue-multiselect.min.css"

/* RESET */
* {
  margin: 0;
  padding: 0;
  border: 0;
  outline: none;
  box-sizing: border-box;
}
/* LAYOUT */
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.toolbar {
  padding: 0.5em;
}
.toolbar-button,
.toolbar-search {
  padding: inherit;
  border-radius: 0.3em;
}
.toolbar-search {
  float: right;
}
.note-container {
  display: flex;
  flex: 1;
}
.note-selectors {
  flex: 0 0 13em;
}
.note-selector {
  padding: 1em;
}
.note-selector p {
  margin: 0;
}
.note-editor {
  display: flex;
  flex: 1;
  flex-direction: column;
}
.note-editor-info {
  padding: 0.5em;
  text-align: center;
}
.note-editor-input {
  display: flex;
  flex: 1;
  width: 100%;
  padding: 0 2em 0 2em;
}
/* COLORS */
* {
  color: #454545;
  background-color: #fafaf8;
}
.toolbar {
  background-color: ##fffff;
}
.toolbar-button {
  background-color: #ffffff;
}
.toolbar-button:active {
  background-color: #aaaaaa;
}
.note-selectors {
  border-right: 1px solid #dcdadc;
}
.note-selector {
  border-bottom: 1px solid #dcdadc;
}
.note-selector.active {
  background-color: #fce18d;
}
.note-selector-title {
  background-color: inherit;
}
.note-selector-timestamp {
  color: #626262;
  background-color: inherit;
}
.note-editor-info {
  color: #dcdadc;
}
/* TYPOGRAPHY */
body {
  font-family: sans-serif;
}
.note-selector-title {
  font-weight: bold;
}
.note-selector-timestamp {
  font-size: 0.7em;
}
.note-editor,
.note-editor-input {
  font-size: 0.9em;
}
</style>
