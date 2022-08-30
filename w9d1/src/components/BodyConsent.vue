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
    <article>
        <div v-for="post in postsList" :key="post.title"> 
            <h2>Título: {{post.title}}</h2>
            <p>Description: {{post.description}}</p>
            <p>{{post.content}}</p>
        </div>
    </article>
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
      postsList: [
        {title: "Number 1", 
        description: "This post number 1 is a.....",
        content: "Post number 1 content",},
        {title: "Number 2", 
        description: "This post number 2 is a.....",
        content: "Post number 2 content",},
        {title: "Number 3", 
        description: "This post number 3 is a.....",
        content: "Post number 3 content",},
        {title: "Number 4", 
        description: "This post number 4 is a.....",
        content: "Post number 4 content",},

      ]
    };
  },
};
</script>

<style>
</style>