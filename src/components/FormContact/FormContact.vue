<template>
    <section>
        <header>
            <h2>{{ name }}</h2>
            <p></p>
        </header>
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

import InputFirstLastName from "./components/InputFirstLastName.vue";
import InputAdressMail from "./components/InputAdressMail.vue";
import InputAboutYou from "./components/InputAboutYou.vue";
import InputInTheFrame from "./components/InputInTheFrame.vue";
import InputComment from "./components/InputComment.vue";
import InputResponseAtTheLatest from "./components/InputResponseAtTheLatest.vue";
import InputSubmit from "./components/InputSubmit.vue";

const name = "FormContact"
</script>

<style scoped lang="scss">
@import "../../assets/main.scss";
section {
    position: relative;
    width: 50%; height: 100vh;
    background-color: map-get($colour, "primary");
    
    header {
        h2 {
            @include font-title-bold--secondary;
        }
    }
    
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