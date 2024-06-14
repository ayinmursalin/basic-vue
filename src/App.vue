<template>
  <LearnConditional msg="Hello Conditional" />
</template>

<script>
import LearnConditional from "./components/LearnConditional.vue";

export default {
  name: "App",
  components: {
    LearnConditional,
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
