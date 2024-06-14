<template>
  <LearnBind msg="Hello Bind" />
  <hr />
  <LearnConditional msg="Hello Conditional" />
</template>

<script>
import LearnBind from "./components/LearnBind.vue";
import LearnConditional from "./components/LearnConditional.vue";

export default {
  name: "App",
  components: {
    LearnBind,
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
