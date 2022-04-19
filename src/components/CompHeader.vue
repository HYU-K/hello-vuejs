<template>
  <header>
    <h1>{{ title }}</h1>
    <button v-on:click="changeTitleHeader">thay doi title</button>
  </header>
</template>

<script>
export default {
  name: "comp-header",

  props: {
    title: String,
  },

  data() {
    return {
      textHeader: "Hello Header",
    };
  },

  methods: {
    changeTitleHeader() {
      this.$emit("changTitleEven");
    },
  },
};
</script>

<style lang="" scoped>
</style>