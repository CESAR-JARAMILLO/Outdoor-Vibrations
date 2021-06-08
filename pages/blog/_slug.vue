<template>
  
  <article>
    <Navbar />
    <img class="main-image" :src="require(`~/assets/${article.img}`)" :alt="article.alt" />
    <h1 class="title">{{ article.title }}</h1>
    <p>Written by</p>
    <hr>
    <nuxt-content :document="article" />
    <p>Article last updated: {{ formatDate(article.updatedAt) }}</p>
    <pre> {{ article }} </pre>
  </article>
</template>

<script>
import Navbar from "../../components/Navbar"

  export default {
    async asyncData({ $content, params }) {
      const article = await $content('articles', params.slug).fetch()

      return { article }
    },
    components: {
      Navbar
    },
    methods: {
    formatDate(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    }
 }
  }
</script>

<style scoped>
  article {
    text-align: center;
  }
  .main-image {
    margin-top: 3rem;
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 60%;
  }

  .title {
    margin-top: 2rem;
    font-size: 52px;
    margin-left: auto;
    margin-right: auto;
    width: 50%;
  }

  hr {
    margin: 1rem auto;
    width: 50%;
  }

  .nuxt-content-container {
    margin-left: auto;
    margin-right: auto;
    width: 50%;
  }

  p {
    margin: 2rem 0;
  }

  .nuxt-content h1 {
    font-weight: bold;
    font-size: 28px;
  }
  .nuxt-content h3 {
    font-weight: bold;
    font-size: 22px;
  }
  .nuxt-content p {
    margin-bottom: 20px;
  }
</style>