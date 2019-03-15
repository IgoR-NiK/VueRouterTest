<template>
    <div>
        <nav-bar v-bind:items="items"></nav-bar>
        <router-view></router-view>
    </div>
</template>

<script>
    module.exports = {
        components: {
            'nav-bar': httpVueLoader('/js/components/nav-bar.vue')
        },
        data: function () {
            return {
                items: [{
                    name: 'SubPage1',
                    path: '/Home/SubPage1'
                }, {
                    name: 'SubPage2',
                    path: '/Home/SubPage2'
                }, {
                    name: 'SubPage3',
                    path: '/Home/SubPage3'
                }]
            }
        }
    };
</script>

<style>

</style>