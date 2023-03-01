<script>

// IMPORT DEL COMPONENTE
import MyComponent from "./components/MyComponent.vue";
import MyOtherComponent from "./components/MyOtherComponent.vue";

// DEFINIZIONE DEL COMPONENTE IN PAGINA
export default {

  components: {
    MyComponent, MyOtherComponent
  },
};
</script>

<template>
  <MyComponent></MyComponent>
  <MyOtherComponent></MyOtherComponent>
</template>


<style lang="scss"></style>