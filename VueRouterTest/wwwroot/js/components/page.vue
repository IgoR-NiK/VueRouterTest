<template>
    <div>
        <nav-bar v-bind:items="['SubPage1', 'SubPage2', 'SubPage3']" v-on:change-item="changeItem"></nav-bar>
        <router-view></router-view>
    </div>
</template>

<script>
    module.exports = {
        components: {
            'nav-bar': httpVueLoader('/js/components/nav-bar.vue')
        },
        methods: {
            changeItem: function (item) {
                this.$router.push({ path: `/home/${item}` });
            }
        }
    };
</script>

<style>

</style>