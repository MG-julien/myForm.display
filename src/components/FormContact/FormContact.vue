<template>
    <section>
      <HeaderForm />
      <form>
        <div class="container__inputFirstLastName">
            <InputNameAndMail
            :componentNodeInput="'firstName__container'"
            :inputType="'text'"
            :inputId="'inputFirstName'"
            :inputName="'firstName'"
            :inputplaceholder="'Nom'"
            :inputMinlength="2"
            :inputMaxlength="50"
            />

            <InputNameAndMail
            :componentNodeInput="'lastName__container'"
            :inputType="'text'"
            :inputId="'inputLastName'"
            :inputName="'lastName'"
            :inputplaceholder="'Prénom'"
            :inputMinlength="2"
            :inputMaxlength="50"
            />
        </div>
        <InputNameAndMail
          :componentNodeInput="'email__container'"
          :inputType="'email'"
          :inputId="'inputEmail'"
          :inputName="'email'"
          :inputplaceholder="'Email'"
          :inputMinlength="5"
          :inputMaxlength="100"
        />
      </form>
    </section>
  </template>
  

<script setup lang="ts">
import HeaderForm from "./components/HeaderForm.vue";
import InputNameAndMail from "./components/InputNameAndMail.vue";

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
         min-width:20%; width: 45%; max-width: 45%;
    }
}
</style>
