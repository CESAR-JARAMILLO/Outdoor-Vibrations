<template>
  <div>
    <Navbar />
    <article>
      <img class="main-image" :src="require(`~/assets/${article.img}`)" :alt="article.alt">
      <h1 class="title">
        {{ article.title }}
      </h1>
      <div class="author">
        <img class="author-image" :src="require(`~/assets/${article.author.image}`)">
        <p>Christina Jules</p>
      </div>
      <hr>
      <nuxt-content :document="article" />
    </article>
  </div>
</template>

<script>
import Navbar from '../../components/Navbar'

export default {
  components: {
    Navbar
  },
  async asyncData ({ $content, params }) {
    const article = await $content('articles', params.slug).fetch()

    return { article }
  }
}
</script>

<style>
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

.author {
  display: flex;
  justify-content: center;
  align-items: center;
}

.author-image {
  height: 40px;
  border-radius: 50%;
  margin-right: 10px;
}

.nuxt-content {
  width: 60%;
  margin: auto;
  text-align: left;
}

.nuxt-content p {
  margin: 28px 0;
}

.nuxt-content h2 {
  font-size: 40px;
  margin-left: 0;
}

.icon.icon-link {
  display: none;
}
</style>
