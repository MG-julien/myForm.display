<template>
    <ul :class="ulClass">
        <li :class="liClass">
            <input 
                :type="inputType"
                :id="inputId"
                :name="inputName"
                :value="inputValue"
            />
            <label :for="inputName">{{ inputValue }}</label>
        </li>
    </ul>
</template>

<script setup lang="ts">

const props = defineProps({
    ulClass: String,
    liClass: String,
    inputType: String,
    inputId: String,
    inputName: String,
    inputValue: String,
});

const { ulClass, liClass, inputType, inputId, inputName, inputValue } = props;

console.log(props)
</script>

<style scoped lang="scss">
@import "../../../assets/main.scss";

ul {
    position: relative;
    width: 100%;
    height: 40px;

    &::before, &::after{
        content: " ";
        position: absolute;
        right: 0%;
        bottom: 0%;
        z-index: 1111;
        width: 10px;
        height: 2px;
        margin-right: 10px;
        margin-bottom: 15px;
        background-color: map-get($colour, "secondary");
        transform: rotate(-45deg);
    }

    &::after {
        margin-right: 16px;
        transform: rotate(45deg);
    }
    
    li {
        width: 100%;
        height: 100%;
        padding-left: 20px;
        line-height: 40px;
        @include font-paragraph-regular;
        border-bottom: 2px solid map-get($colour, "secondary");

        label {
            padding-left: 10px;
            @include font-paragraph-regular;
            color: map-get($colour, "secondary");
        }
    }
}
</style>