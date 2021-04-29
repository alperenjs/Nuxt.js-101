<template>
  <div>
    <nuxt-link to="/jokes">
      <span class="backlink"> Back to Jokes Bitch </span></nuxt-link
    >
    <h2>{{ joke }}</h2>
    <small>Joke ID: {{ $route.params.id }}</small>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      joke: {},
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };
    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config
      );
      this.joke = res.data.joke;
    } catch (error) {
      console.log(error);
    }
  },
  head() {
    return {
      title: "Was Funny Right?",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "jokes, best place for funny dad jokes",
        },
      ],
    };
  },
};
</script>

<style>
.backlink {
  color: rgb(34, 112, 184);
}
</style>