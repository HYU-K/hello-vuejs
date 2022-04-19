<template>
    <div class="user">
        <p>{{ user.email }}</p>
        <button v-on:click="handleDelete" class="delete">delete</button>
    </div>
</template>

<script>
export default {
    name: 'proUser',
    props: {
        user: {
            type: Object,
            default: null
        }
    },
    data() {
        return {}
    },
    methods: {
        handleDelete(e) {
            var data = {
                id: this.user.id
            };
            this.$emit('deleteUser', data);
             console.log(e)
        }
    }
}
</script>

<style>
    .user {
        display: flex;
        align-items: center;
        justify-content: center
    }

    .delete {
        margin-left: 15px;
    }
</style>