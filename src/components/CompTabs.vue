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
    name: 'comp-tabs',
    props: {
        title: String
    },
    data() {
        return {}
    },
    methods: {
    }
}
</script>

<style>

</style>