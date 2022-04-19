<template>
  <div class="Demo-slot">
    <h1>demo slot</h1>
    <comp-tabs title="Tiêu đề của tabs">
      <ul class="tabs-header">
        <li
          v-for="(item, index) in tapsHeader"
          v-bind:key="index"
          v-on:click="setActivetabs(index)"
          v-bind:class="{ active: tabActive == index }"
        >
          {{ item.text }}
        </li>
      </ul>
      <div class="item-content">
        <div class="content tab1" v-if="tabActive === 0">
          <h3>tab 1</h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum,
            natus quia, nobis, obcaecati perspiciatis laboriosam aut veniam
            repellendus voluptatibus fugit voluptatum impedit! Cumque fugit
            natus necessitatibus voluptates nesciunt rerum veritatis!
          </p>
          <p>
            quia, nobis, obcaecati perspiciatis laboriosam aut veniam
            repellendus voluptatibus fugit voluptatum imp
          </p>
        </div>
        <div class="content tab1" v-else-if="tabActive === 1">
          <h3>tab 2</h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum,
            natus quia, nobis, obcaecati perspiciatis laboriosam aut veniam
            repellendus voluptatibus fugit voluptatum impedit! Cumque fugit
            natus necessitatibus voluptates nesciunt rerum veritatis!
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum,
            natus quia, nobis, obcaecati perspiciatis laboriosam aut veniam
            repellendus voluptatibus fugit voluptatum impedit! Cumque fugit
            natus necessitatibus voluptates nesciunt rerum veritatis!
          </p>
        </div>
        <div class="content tab1" v-else>
          <h3>tab 3</h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum,
            natus quia, nobis, obcaecati perspiciatis laboriosam aut veniam
            repellendus voluptatibus fugit voluptatum impedit! Cumque fugit
            natus necessitatibus voluptates nesciunt rerum veritatis!
          </p>
        </div>
      </div>
    </comp-tabs>
  </div>
</template>

<script>
import CompTabs from "./CompTabs.vue";
export default {
  name: "Demo-slot",
  data() {
    return {
      tapsHeader: [{ text: "tab 1" }, { text: "tab 2" }, { text: "tab 3" }],
      tabActive: 0,
    };
  },
  methods: {
    setActivetabs(index) {
      console.log(index);
      this.tabActive = index;
    },
  },
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