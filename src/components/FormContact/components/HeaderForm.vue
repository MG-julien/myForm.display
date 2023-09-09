<template>
    <header>
            <h2>{{ titleHeader }}</h2>
            <p>{{ paraHeader }}</p>
        </header>
</template>

<script setup lang="ts">

const titleHeader = "Me contacter"
const paraHeader = "Les données qui me sont transmises sont bien évidemment confidentielles. Je m’engage personnellement à ne pas divulguer vos données personnelles saisies dans ce formulaire."

</script>

<style scoped lang="scss">
@import "../../../assets/main.scss";
header {
        h2 {
            width: 100%; height: 60px;
            @include font-title-bold--secondary;
        }
        p {
            width: 100%; height: 80px;
            @include font-infoBubble-regular
        }
    }
</style>