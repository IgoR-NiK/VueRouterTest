<template>
    <div class="flex-container">
        <page class="flex-item"></page>
        <page class="flex-item"></page>
    </div>
</template>

<script>
    module.exports = {
        components: {
            'page': httpVueLoader('/js/components/page.vue')
        },
    };
</script>

<style>
    .flex-container {
        display: flex;
    }
</style>