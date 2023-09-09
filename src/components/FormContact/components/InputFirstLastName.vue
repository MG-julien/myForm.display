<template>
    <div :class="attrMainContainer">
        <div :class="attrFirstNameInput.attrContainer">
            <input v-bind="attrFirstNameInput.checkbox"/>
            <label v-bind="attrFirstNameInput.label">{{ attrFirstNameInput.label.text }}</label>
            <input v-bind="attrFirstNameInput.text" />
        </div>
        <div :class="attrLastNameInput.attrContainer">
            <input v-bind="attrLastNameInput.checkbox"/>
            <label v-bind="attrLastNameInput.label">{{ attrLastNameInput.label.text }}</label>
            <input v-bind="attrLastNameInput.text" />
        </div>
    </div>
</template>

<script setup lang="ts">
const attrMainContainer = "inputFirstLastName__container";
const attrFirstNameInput = {
    attrContainer: "firstNameInput__container",    
    text: { id: "inputTextFirstName", type: "text", name: "firstName", placeholder: "nom" },
    checkbox: { id: "inputCheckFirstName", type: "checkbox", for: "firstName" },
    label: {  id: "labelCheckFirstName", for: "firstName", text: "nom"},
};
const attrLastNameInput = {
    attrContainer: "lastNameInput__container",    
    text: { id: "inputTextLastName", type: "text", name: "lastName", placeholder: "prénom" },
    checkbox: { id: "inputCheckLastName", type: "checkbox", for: "lastName" },
    label: { id: "labelCheckLastName", for: "lastName", text: "prénom" },
};

</script>

<style scoped lang="scss">
@import "../../../assets/main.scss";
.inputFirstLastName__container {
    display: flex;
    width: 100%; height: 40px;
    justify-content: space-between;
    margin-bottom: 40px;
 
    .firstNameInput__container, .lastNameInput__container{
        position: relative;
        max-width: 250px; width: 250px; height: 100%;
        border-bottom: 2px solid map-get($colour, "secondary");
    }
    
    #inputCheckFirstName, #inputCheckLastName {
        position: absolute; z-index: 2;
        bottom: 0%; left: 0%;
        margin-bottom: 10px;
        width: 10px; height:20px;
        border: 2px solid black;
    }
    /**
    #inputCheckFirstName, #inputCheckLastName {
        position: absolute; z-index: 2;
        bottom: 0%; left: 0%;
        margin-bottom: 10px;
        @include button-checkbox(map-get($colour, "secondary"), map-get($colour, "primary"));
    }

     #inputCheckFirstName:checked, #inputCheckLastName:checked {
        position: absolute; z-index: 2;
        bottom: 0%; left: 0%;
        margin-bottom: 10px;
        appearance: none;
        @include button-checkbox(map-get($colour, "secondary"), map-get($colour, "quaternary"));
    }
     */

        #inputTextFirstName, #inputTextLastName {
            position: absolute; z-index: 1;
            width:100%; height: 100%;
            padding-left: 20px;
            @include font-paragraph-regular;
            background-color: map-get($colour, "primary");
        }
        #labelCheckFirstName, #labelCheckLastName {
            position: absolute;
        }
}
</style>