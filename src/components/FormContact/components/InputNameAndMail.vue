<template>
    <div :class="attrContainerParents.containerRoot">
      <div class="attrContainerParents.containerFirstLastName">
        <div :class="attrContainerParents.containerFirstLastName.firstNameChildNode">
          <input :class="attrFirstNameInput.checkbox" />
          <label :class="attrFirstNameInput.label">{{ attrFirstNameInput.label.text }}</label>
          <input :class="attrFirstNameInput.text" />
        </div>
        <div :class="attrContainerParents.containerFirstLastName.lastNameChildNode">
          <input :class="attrLastNameInput.checkbox" />
          <label :class="attrLastNameInput.label">{{ attrLastNameInput.label.text }}</label>
          <input :class="attrLastNameInput.text" />
        </div>
      </div>
      <div :class="attrContainerParents.containerAdressMail">
        <input :class="attrAdressMailInput.checkbox" />
        <label :class="attrAdressMailInput.label">{{ attrAdressMailInput.label.text }}</label>
        <input :class="attrAdressMailInput.text" />
      </div>
    </div>  
  </template>
  

<script setup lang="ts">
const attrContainerParents = {
    containerRoot: "componentRoot__firstLastNameMail",
    containerFirstLastName: {
        parentNode: "firstAndLastName__container",
        firstNameChildNode: "firstName__container",
        lastNameChildNode: "lastName__container",
    },
    containerAdressMail: "adressMail__container",
}
const attrFirstNameInput = {  
    text: { id: "inputTextFirstName", type: "text", name: "firstName", placeholder: "nom" },
    checkbox: { id: "inputCheckFirstName", type: "checkbox", for: "firstName" },
    label: {  id: "labelCheckFirstName", for: "firstName", text: "nom"},
};
const attrLastNameInput = {  
    text: { id: "inputTextLastName", type: "text", name: "lastName", placeholder: "prénom" },
    checkbox: { id: "inputCheckLastName", type: "checkbox", for: "lastName" },
    label: { id: "labelCheckLastName", for: "lastName", text: "prénom" },
};
const attrAdressMailInput = {
    text: { id: "inputTextAdressMail", type: "email", name: "email", placeholder: "jean-de-croix@gmail.com" },
    checkbox: { id: "inputCheckAdressMail", type: "checkbox", for: "email" },
    label: { id: "labelCheckAdressMail", for: "email", text: "email" },
};

</script>

<style scoped lang="scss">
@import "../../../assets/main.scss";
.firstAndLastName__container {
    display: flex;
    width: 100%; height: 40px;
    justify-content: space-between;
    margin-bottom: 40px;
 
    .firstName__container, .lastName__container{
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

  