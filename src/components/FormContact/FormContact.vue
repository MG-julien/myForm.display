<template>
    <section>
        <HeaderForm />
        <form>
            <InputNameAndMail />
            <InputAboutYou />
            <InputInTheFrame />
            <InputComment />
            <InputResponseAtTheLatest />
            <InputSubmit />
        </form>
    </section>
</template>

<script setup lang="ts">

import HeaderForm from "./components/HeaderForm.vue";
import InputNameAndMail from "./components/InputNameAndMail.vue";
import InputAboutYou from "./components/InputAboutYou.vue";
import InputInTheFrame from "./components/InputInTheFrame.vue";
import InputComment from "./components/InputComment.vue";
import InputResponseAtTheLatest from "./components/InputResponseAtTheLatest.vue";
import InputSubmit from "./components/InputSubmit.vue";

</script>

<style scoped lang="scss">
@import "../../assets/main.scss";
section {
    position: relative;
    width: 50vw; height: 100vh;
    padding: 80px;
    background-color: map-get($colour, "primary");
    
    form {
        display: flex;
        flex-direction: column;
    }
}

</style>