<template>
    <section>
        <HeaderForm />
        <form>
            <div class="container__inputFirstLastName">
                <InputNameAndMail
                    :classComponentContainer="'firstName__container'"
                    :inputType="'text'"
                    :inputId="'inputFirstName'"
                    :inputName="'firstName'"
                    :inputplaceholder="'Nom'"
                    :inputMinlength="2"
                    :inputMaxlength="50"
                />
                <InputNameAndMail
                    :classComponentContainer="'lastName__container'"
                    :inputType="'text'"
                    :inputId="'inputLastName'"
                    :inputName="'lastName'"
                    :inputplaceholder="'Prénom'"
                    :inputMinlength="2"
                    :inputMaxlength="50"
                />
            </div>
            <InputNameAndMail
                :classComponentContainer="'email__container'"
                :inputType="'email'"
                :inputId="'inputEmail'"
                :inputName="'email'"
                :inputplaceholder="'Email'"
                :inputMinlength="5"
                :inputMaxlength="100"
            />
            <div class="containerDropDown--who">
                <label>Vous êtes :</label>
                <DropDownInput
                    :ulClass="'dropDrop__container'"
                    :liClass="'dropDrop__container__li'"
                    :inputType="'checkbox'"
                    :inputId="'...'"
                    :inputName="'...'"
                    :inputValue="'entreprise'"
                />
                <DropDownInput
                :ulClass="'dropDrop__container'"
                    :liClass="'dropDrop__container__li'"
                    :inputType="'checkbox'"
                    :inputId="'...'"
                    :inputName="'...'" 
                    :inputValue="'secteur'"
                />
            </div>
            <div class="containerDropDown--why">
                <label>Vous me contactez dans le cadre :</label>
                <DropDownInput
                    :ulClass="'dropDrop__container'"
                    :liClass="'dropDrop__container__li'"
                    :inputType="'checkbox'"
                    :inputId="'...'"
                    :inputName="'...'"
                    :inputValue="'d\'une mission'"
                />
            </div>
        </form>
    </section>
  </template>
  

<script setup lang="ts">
import HeaderForm from "./components/HeaderForm.vue";
import InputNameAndMail from "./components/InputNameAndMail.vue";
import DropDownInput from "./components/DropDownInput.vue";
import { reactive } from "vue";

const dropDownWho = reactive({
    activity : { 
        campany: { inputId:"selectCompany", inputName:"company", inputValue:"entreprise",},
        startup: { inputId:"selectStartup", inputName:"startup", inputValue:"startup",},
        individual: { inputId:"selectIndividual", inputName:"individual", inputValue:"particulier",},
        another: { inputId:"selectAnother", inputName:"another", inputValue:"autre",},
    },
    activityArea: {
        inputId:"",
        inputName:"",
        inputValue:"",
    }
})
</script>

<style scoped lang="scss">
@import "../../assets/main.scss";
section {
    position: relative;
    width: 50vw; height: 100vh;
    padding: 80px;
    background-color: map-get($colour, "primary");
}
.container__inputFirstLastName {
    width: 100%; max-width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-bottom: 20px;
    .firstName__container, .lastName__container {
        width: 50%;
    }
    .firstName__container {
        margin-right: 15px;
    }
    .lastName__container {
        margin-left: 15px;
    }
}
.containerDropDown--who, .containerDropDown--why {
    width: 100%;
    height: 40px;
    display: flex;
    margin-top: 20px;

    label {
        line-height: 40px;
        @include font-paragraph-regular-bold; 
    }
    .dropDrop__container {
        flex: 1;
        min-width:20%; width: 100%;
        margin-left: 30px;
    }
}
</style>
