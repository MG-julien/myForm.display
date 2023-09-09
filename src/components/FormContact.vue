<template>
    <h2>{{ name }}</h2>
</template>

<script setup lang="ts">
const name = "FormContact"
</script>

<style scoped lang="scss">
@import "../assets/main.scss";

h2{
    width: 50%; height: 100vh;
    @include font-title-bold--secondary;
    background-color: map-get($colour, "primary");
}
</style>