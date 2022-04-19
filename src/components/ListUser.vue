<template>
  <div class="List-user">
    <user v-for="user in listUser" v-bind:key="user.id" v-bind:user="user" v-on:deleteUser="deleteUser"/>
  </div>
</template>

<script>
import User from "./User.vue";

export default {
  name: "List-user",
  props: {
    listUser: {
      // type: Array,
      // default: []
    }
  },

  data() {
    return {};
  },

  components: {
    User,
  },

  methods: {
    deleteUser(data) {
      this.$emit('deleteUserEven', data);
    }
  }
};
</script>

<style scoped>
</style>
