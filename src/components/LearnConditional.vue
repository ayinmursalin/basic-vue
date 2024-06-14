<template>
  <div>
    <div v-if="age === 0">This is Zero</div>
    <div v-else-if="age < 0">This Number is Negative</div>
    <div v-else-if="age > 0">This Number is Positive</div>
    <div v-else>This is not a Number</div>

    <div v-show="isOld">
      <button>Buy Ciggerete</button>
      <button v-bind:disabled="age < 30">Buy House</button>
    </div>

    <div align="left">
      <p>Items:</p>
      <ul>
        <li v-for="(x, idx) in items" :key="idx">{{ x }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "LearnConditional",
  props: {
    msg: String,
  },
  data() {
    return {
      age: 22,
      items: ["A", "B", "C"],
    };
  },
  computed: {
    isOld() {
      return this.age >= 21;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
