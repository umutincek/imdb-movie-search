<template>
    <div class="position-absolute w-100 h-100 cutomBg">
        <b-spinner variant="primary" label="Spinning"></b-spinner>
    </div>
</template>

<script>
    export default {
        name: "loading.vue"
    }
</script>

<style scoped>
    .cutomBg {
        background-color: rgba(0,0,0, .20);
        z-index: 99;
        text-align: center;
        padding: 30px;
    }
</style>
