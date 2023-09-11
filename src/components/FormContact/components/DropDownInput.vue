<template>
    <ul :class="props.ulClass">
        <li :class="props.liClass">
            {{ props.liTextValue }}
        </li>
    </ul>
</template>

<script setup lang="ts">
const props = defineProps({
    ulClass: String,
    liClass: String,
    liTextValue: String,
    inputType: String,
    inputId: String,
    inputName: String,
})
</script>

<style scoped lang="scss">
@import "../../../assets/main.scss";

ul {
    width: 100%;
    height: 40px;
    
    li {
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: space-between;
        padding-left: 20px;
        line-height: 40px;
        @include font-paragraph-regular;
        border-bottom: 2px solid map-get($colour, "secondary");
    }
}
</style>