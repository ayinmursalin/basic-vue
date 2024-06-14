<template>
  <div>Message from app: {{ msg }}</div>
  <div>{{ innerMessage }} is from Component</div>

  <div>
    <div v-bind:id="containerId">V Bind ID</div>
    <div v-bind:class="simpleClass">V Bind Class</div>
    <div v-bind:class="[isImportant ? 'important' : 'simple']">
      V Bind Class Conditional
    </div>
    <img v-bind:src="dbImage" alt="Some Image from DB" />
    <div
      v-bind:style="{
        backgroundColor: 'green',
        fontSize: customStyleFontSize + 'px',
        color: 'white',
      }"
    >
      This Is V Bind Style
    </div>
    <div :class="simpleClass" :style="{ border: '2px solid red' }">V Bind Short Hand</div>
  </div>
</template>

<script>
export default {
  name: "LearnBind",
  props: {
    msg: String,
  },
  data() {
    return {
      innerMessage: "Hehehehe",
      containerId: "header",
      simpleClass: "simple",
      isImportant: true,
      dbImage:
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRL5m2gr2lMb1huhMFwIR41jrDU5ZOxKydgEw&s",
      customStyleFontSize: 32,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#header {
  padding: 20px;
  background-color: blue;
  color: white;
}

.simple {
  font-size: 24px;
  background-color: yellow;
}

.important {
  font-size: 24px;
  font-style: italic;
  font-weight: bold;
  background-color: green;
}
</style>
