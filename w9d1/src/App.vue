<template>
  <div>
    <header>
      <NavBar></NavBar>
    </header>
    <Footer @updateEmail="updateEmail" @update="updateName" :nameInput="nameInput" :emailInput="emailInput"></Footer>
    <BodyConsent :nameInput="nameInput" :emailInput="emailInput"></BodyConsent>
  </div>
  </template>

<script>
import Footer from "./components/Footer.vue";
import NavBar from "./components/NavBar.vue";
import BodyConsent from "./components/BodyConsent.vue";
export default {
  name: "app",
  components: {
    NavBar,
    Footer,
    BodyConsent,
  },
  data() {
        return {
            nameInput: "",
            emailInput: "",
        }
    },
    methods: {
      updateName(value) {
        this.nameInput = value;
      },
      updateEmail(value){
          this.emailInput = value;
        }
    }
};
</script>
<style></style>
