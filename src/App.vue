<script setup lang="ts">
import AboutForm from "./components/AboutForm.vue";
import FormContact from "./components/FormContact/FormContact.vue";
</script>

<template>
  <div>
    <AboutForm />
    <FormContact />
  </div>
</template>

<style scoped lang="scss">
@import "./assets/main.scss";

div{
  width: 100%;
  display: flex;
 }
</style>