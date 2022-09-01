<template>
  <div>
    <header>
      <NavBar></NavBar>
    </header>
    <Footer
      @updateEmail="updateEmail"
      @update="updateName"
      :nameInput="nameInput"
      :emailInput="emailInput"
    ></Footer>
    <BodyConsent :nameInput="nameInput" :emailInput="emailInput"></BodyConsent>
  </div>

  <hr />
  <hr />
  <h2>Formulario nuevo con v-model</h2>
  <form action="/some-url" method="get">
    <NewForm v-model="name" placeholder="Name"/>
    <NewForm v-model="surname" placeholder="Surname"/>
    <NewForm v-model="number" type="number" placeholder="Number"/>
    <NewForm type="submit" value="Send"/>
  </form>

  <div>
    <h2>El padre se entera?</h2>
    <div>Name: {{name}}</div>
    <div>Surname: {{surname}}</div>
    <div>Number: {{number}}</div>
  </div>
</template>


<script>
import Footer from "./components/Footer.vue";
import NavBar from "./components/NavBar.vue";
import BodyConsent from "./components/BodyConsent.vue";
import NewForm from "./components/NewForm.vue";

export default {
  name: "app",
  components: {
    NavBar,
    Footer,
    BodyConsent,
    NewForm,
  },
  data() {
    return {
      nameInput: "",
      emailInput: "",
      name: null,
      surname: null,
      number: null,
    };
  },
  methods: {
    updateName(value) {
      this.nameInput = value;
    },
    updateEmail(value) {
      this.emailInput = value;
    },
  },
};
</script>
<style></style>
