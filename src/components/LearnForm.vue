<template>
  <p>Hello from App, {{ msg }}</p>
  <form v-on:submit.prevent="addItem">
    <p>Add Item</p>
    <p>Item Name: <input type="text" required v-model="itemName" /></p>
    <p>How Many: <input type="number" required v-model="itemCount" /></p>
    <button type="submit">Submit</button>
  </form>

  <hr />
  <div>
    <p>Items:</p>
    <ol>
      <li v-for="(item, idx) in items" :key="idx">
        {{ item.name }} ({{ item.count }} pcs)
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: "LearnForm",
  props: {
    msg: String,
  },
  data() {
    return {
      itemName: null,
      itemCount: null,
      items: [],
    };
  },
  methods: {
    addItem() {
      let item = {
        name: this.itemName,
        count: this.itemCount,
      };

      this.items.push(item);
      this.itemName = null;
      this.itemCount = null;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
