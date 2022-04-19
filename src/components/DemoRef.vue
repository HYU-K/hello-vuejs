<template>
    <div class="Demo-ref">
        <h1>demoref</h1>
        <button v-on:click="handleclickinput" class="">thay đổi avt</button>
        <input ref="fileinputAvt" type="file" style="display: none;">
    </div>
</template>

<script>
export default {
    name: 'Demo-ref',
    data() {
        return {}
    },
    methods: {
        handleclickinput(e) {
            this.$refs.fileinputAvt.click(e);
        }
    }
}
</script>

<style>

</style>