<template>
    <div :class="props.componentNodeInput" >
        <label :for="props.inputId">{{ props.inputplaceholder }}</label>
        <input 
            :type="props.inputType" 
            :id="props.inputId" 
            :name="props.inputName" 
            :placeholder="props.inputplaceholder" 
            :minlength="props.inputMinlength"
            :maxlength="props.inputMaxlength"
        />
    </div>
</template>
  

<script setup lang="ts">

const props = defineProps({
    componentNodeInput: String,
    inputType: String,
    inputId: String,
    inputName: String,
    inputplaceholder: String,
    inputMinlength: Number,
    inputMaxlength: Number,
})
console.log(props);

</script>

<style scoped lang="scss">
@import "../../../assets/main.scss";

div {
    width: 100%;
    height: 40px;
    display: flex;
    flex-direction: row;
    align-items: center;
    border-bottom: 2px solid map-get($colour, "secondary");
    
    label {
      line-height: 40px;
      @include font-paragraph-regular;
    }

    input {
      flex: 1; /* L'input prend le reste de l'espace disponible */
      width: 100%;
      height: 100%;
      padding-left: 20px;
      @include font-paragraph-regular;
      background-color: map-get($colour, "primary");
      outline: transparent;
    }

    input::placeholder {
      color: transparent;
    }
}

input:focus::placeholder {
    color: map-get($colour-rgba, "secondary")
}
    
div:focus-within {
    transition-duration: 200ms;
    border-bottom: 8px solid map-get($colour-rgba, "secondary");
    border-bottom-left-radius: 4px;
    border-bottom-right-radius: 4px;
}
</style>

  