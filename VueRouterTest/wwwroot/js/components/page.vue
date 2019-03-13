<template>
    <div>
        <nav-bar v-bind:items="['SubPage1', 'SubPage2', 'SubPage3']" v-on:change-item="changeItem"></nav-bar>
        <router-view></router-view>
    </div>
</template>

<script>
    var baseItem = httpVueLoader('/js/components/base-item.vue');

    module.exports = {
        components: {
            'nav-bar': httpVueLoader('/js/components/nav-bar.vue')
        },
        methods: {
            changeItem: function (item) {

                this.$router.replace({ path: `/page/${item}` });
            }
        },
        router: new VueRouter({
            mode: 'history',
            routes: [
                { path: '/page', component: baseItem },
              //  { path: '/home', component: homeItem },
                { path: '/page/:label', component: baseItem }
            ]
        })
    };
</script>

<style>

</style>