<template>
  <div id="app">
    <comp-header v-bind:title="title" v-on:changTitleEven="handlChangeTitle" />
    <List-user
      v-on:deleteUserEven="handleDeleteUser"
      v-bind:listUser="listUser"
    />
    <comp-footer v-bind:title="title" />
    <Demo-ref />
    <demo-slot />
  </div>
</template>

<script>
import CompHeader from "./components/CompHeader.vue";
import CompFooter from "./components/CompFooter.vue";
import ListUser from "./components/ListUser.vue";
import DemoRef from "./components/DemoRef.vue";
import DemoSlot from './components/DemoSlot.vue';

export default {
  name: "App",
  data() {
    return {
      title: "hello vue - hello world",
      listUser: [
        { id: 101, email: "test1@gmail.com", active: true },
        { id: 102, email: "test2@gmail.com", active: false },
        { id: 103, email: "test3@gmail.com", active: true },
        { id: 104, email: "test4@gmail.com", active: false },
        { id: 105, email: "test5@gmail.com", active: true },
        { id: 106, email: "test6@gmail.com", active: true },
      ],
    };
  },

  components: {
    CompHeader,
    ListUser,
    CompFooter,
    DemoRef,
    DemoSlot,
  },

  methods: {
    handlChangeTitle() {
      this.title = "Title thay đổi => do header";
    },

    handleDeleteUser(data) {
      var indexDelete = -1;
      this.listUser.forEach((u, idx) => {
        if (u.id === data.id) {
          indexDelete = idx;
        }
      });

      if (indexDelete != -1) {
        this.listUser.splice(indexDelete, 1);
      }
      console.log(data);
    },
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
