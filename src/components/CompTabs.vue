<template>
  <div class="comp-tabs">
    <div class="tabs-title">
      <span>{{ title }}</span>
    </div>
    <div class="tabs-content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "comp-tabs",
  props: {
    title: String,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style>
.tabs-header {
  display: flex;
  align-items: center;
  padding: 0;
}

.tabs-header li {
  display: inline-block;
  padding: 5px 10px;
  background-color: #ccc;
  cursor: pointer;
  color: black;
}

.tabs-header li:hover {
  background-color: black;
  color: white;
}

.tabs-header .active {
  background-color: black;
  color: white;
}

.item-content {
  border: 1px solid black;
  padding: 20px;
}

.item-content .content {
  text-align: left;
}
</style>