<template>
  <LearnForm msg="Hello Form" />
</template>

<script>
import LearnForm from "./components/LearnForm.vue";

export default {
  name: "App",
  components: {
    LearnForm,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
