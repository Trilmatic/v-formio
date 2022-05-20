<template>
  <div>
    <button @click="$refs.file.validate()">Validate</button>
  </div>
  <formio-file
    ref="file"
    :drop="true"
    :multiple="true"
    :required="true"
    title="Upload File"
    accept=".png"
  ></formio-file>
</template>

<script>
import FormioFile from "./components/FormioFile.vue";

export default {
  name: "App",
  components: {
    FormioFile,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  padding: 2rem;
}

.formio--file-input {
  display: none;
}

.formio--label {
  margin-bottom: 0.5rem;
}

.formio--required {
  margin-left: 0.25rem;
  color: red;
}

.formio--validation-error {
  color: red;
}

.formio--selected-file-icon {
  margin-right: 0.25rem;
}

.formio--selected-file-remove {
  margin-left: 0.25rem;
}

.formio--file.formio--no-drop {
  display: inline-block;
}

.formio--drop-zone .formio--file-view {
  background: #fafafa;
  padding: 30px;
  border: 1px dashed #e7e7e7;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: 0.3s;
  text-align: center;
  margin-bottom: 0.5rem;
}

.formio--selected-file {
  margin-bottom: 0.25rem;
}

.formio--drop-zone .formio--file-view:hover {
  border: 1px dashed #24acf8;
}

.formio--no-drop .formio--file-view {
  display: flex;
  justify-content: space-around;
  align-items: center;
  color: #152a47;
  background: #fafafa;
  text-align: center;
  vertical-align: middle;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  border: 0 solid transparent;
  line-height: 1.6;
  border-radius: 4px;
  padding: 12px 30px;
  margin-bottom: 0.5rem;
  box-shadow: 0 1px 2px 0 rgb(0 0 0 / 24%);
  transition: background-color 0.15s ease-in-out, border-color 0.15s ease-in-out,
    box-shadow 0.15s ease-in-out;
}
</style>
