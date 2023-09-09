<template>
    <section>
        <HeaderForm />
        <form>
            <InputFirstLastName />
            <InputAdressMail />
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
import InputFirstLastName from "./components/InputFirstLastName.vue";
import InputAdressMail from "./components/InputAdressMail.vue";
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
        
        input{
            display: block;
            border: 2px solid black;
        }
    }
}

</style>