<template>
  <div class="Demo-slot">
    <h1>demo slot</h1>
    <comp-tabs title="Tiêu đề của tabs">
        <ul class="tabs-header">
            <li v-for="(item, index) in tapsHeader" v-bind:key="index">
                {{ item.text }}
            </li>
        </ul>
    </comp-tabs>
  </div>
</template>

<script>
import CompTabs from "./CompTabs.vue";
export default {
  name: "Demo-slot",
  data() {
    return {
        tapsHeader: [
            {text: 'tab 1'},
            {text: 'tab 2'},
            {text: 'tab 3'},
        ]
    }
  },
  methods: {},
  components: {
    CompTabs,
  },
};
</script>

<style>
.Demo-slot {
    width: 800px;
    margin: 20px auto;
    padding: 50px;
    border: 1px solid #000;
}
</style>