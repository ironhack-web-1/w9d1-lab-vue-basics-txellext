<template>
  <body>
    <header>
      <NavBar></NavBar>
    </header>
    <Footer></Footer>
  </body>
</template>

<script>

import Footer from "./components/Footer.vue";
import NavBar from "./components/NavBar.vue";
export default {
    name: 'app',
    components: {
    NavBar,
    Footer,
    },
};
</script>

<style>
</style>