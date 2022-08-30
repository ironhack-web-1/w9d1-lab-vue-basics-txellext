<template>
  <div>
    <div>
      <div v-if="nameInput !== ''">{{ confirmationWord + nameInput }}</div>
      <div v-else="nameInput === ''">{{ negationWord }}</div>
    </div>
    <div>
      <div v-if="emailInput !== ''">{{ correctEmail + nameInput }}</div>
      <div v-else="emailInput === ''">{{ negationEmail }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BodyConsent",
  props: ["nameInput", "emailInput"],
  data() {
    return {
      confirmationWord: "Gracias ",
      negationWord: "Your name is mandatory",
      correctEmail: "Gracias por el correo ",
      negationEmail: "Your email is mandatory",
    };
  },
};
</script>

<style>
</style>