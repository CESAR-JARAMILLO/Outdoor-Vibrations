<template>
  
  <article>
    <Navbar />
    <h1>{{ article.title }}</h1>
    <p>{{ article.description }}</p>
    <img :src="require(`~/assets/${article.img}`)" :alt="article.alt" />
    <p>Article last updated: {{ formatDate(article.updatedAt) }}</p>
    <nav>
  <ul>
    <li v-for="link of article.toc" :key="link.id">
      <NuxtLink :to="`#${link.id}`">{{ link.text }}</NuxtLink>
    </li>
  </ul>
</nav>
    <nuxt-content :document="article" />
    <author :author="article.author" />
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

<style>
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