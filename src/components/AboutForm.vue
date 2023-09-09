<template>
    <h2>{{ name }}</h2>
</template>
<script setup lang="ts">
    const name = "AboutFom"
</script>
<style scoped lang="scss">
@import "../assets/main.scss";
h2{
    position: relative;
    width: 50vw; height: 100vh;
    @include font-title-bold--primary;
    background-color: map-get($colour, "secondary");
}
</style>