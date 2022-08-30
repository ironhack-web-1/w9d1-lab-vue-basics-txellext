<template>
  <div>
    <h2>This is my form:</h2>
        <input v-model="nameInput" placeholder="Name"/> 

        <input v-model="emailInput" placeholder="e-mail"/> 

    <h2>This is the two-day-data-binding result:</h2>
        <p>Your name is: {{ nameInput }} </p>
        <p>Your email is: {{ emailInput }} </p>
  </div>
</template>

<script>

export default {
    props: ["nameInput", "emailInput"],
    watch: {
        nameInput(value){
            this.$emit("update", value)
        },
        emailInput(value){
            this.$emit("updateEmail", value)
        }

    }

}
</script>

<style>

</style>