<template>
    <router-link to="/" class="vue-header">
        <h2 class="logo-title">Test Task</h2>
    </router-link>
</template>

<script>
    export default {
        name: "vue-header"
    }
</script>

<style scoped>
    .vue-header {
        position: fixed;
        padding: 31px 48px;
        width: 100%;
        left: 0px;
        top: 0px;
        background: #292D32;
        box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
        text-align: left;
        z-index: 1;
    }

    .logo-title {
        font-family: 'Roboto';
        font-style: normal;
        font-weight: 700;
        font-size: 32px;
        line-height: 38px;
        color: #FFFFFF;
        cursor: pointer;
    }
</style>