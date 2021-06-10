<template>
  <div>
    <Navbar />
    <NuxtLink to="blog/my-first-blog-post">
      <div class="featured">
        <div class="featured-text">
          <p class="featured-category">
            Featured
          </p>
          <h2 class="featured-title">
            {{ articles[0].title }}
          </h2>
          <p class="featured-date">
            May 12, 2021
          </p>
        </div>
        <div class="featured-image" />
      </div>
    </NuxtLink>
    <div class="blog-cards">
      <div v-for="article of articles" :key="article.slug" class="card">
        <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }">
          <div class="card-image">
            <figure class="image is-4by3">
              <img :src="require(`~/assets/${article.img}`)" alt="Placeholder image">
            </figure>
          </div>
          <div class="card-content">
            <div class="media">
              <div class="media-content">
                <p class="card-category title is-6">
                  {{ article.category }}
                </p>
              </div>
            </div>
            <div class="content">
              <p class="card-title title is-4">
                {{ article.title }}
              </p>
              <time class="card-date" datetime="2016-1-1">Jan 1, 2016</time>
            </div>
          </div>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from '../components/Navbar'
export default {
  name: 'Blogs',
  components: {
    Navbar
  },
  async asyncData ({ $content, params }) {
    const articles = await $content('articles')
      .only(['title', 'description', 'img', 'slug', 'author', 'category'])
      .sortBy('createdAt', 'asc')
      .fetch()

    return {
      articles
    }
  }
}
</script>

<style scoped>
.featured {
    display: flex;
    justify-content: center;
    margin-top: 40px;
    font-family: 'Roboto', sans-serif;
}

.featured-text {
    height: 350px;
    width: 600px;
    background-color: #40916c;
    padding-left: 30px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}

.featured-category {
    font-size: 16px;
    font-weight: 500;
    color: #1b4332;
}

.featured-title {
    font-size: 48px;
    font-weight: 600;
    color: #fff;
}

.featured-date {
    font-size: 16px;
    font-weight: 400;
    color: #e6e6e6;
}

.featured-image {
    height: 350px;
    width: 600px;
    background-image: url('~@/assets/autumn.png');
}

.blog-cards {
    margin: 0 10%;
    margin-top: 60px;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 2rem;
    /* justify-content: space-around; */
    /* align-content: space-around; */
}

.card-content {
    background-color: #1b4332;
    font-family: 'Roboto', sans-serif;
    height: 220px;
}

.card-category {
    color: #fff;
}

.card-title {
    color: #fff;
}

.card-date {
    padding-top: 10px;
    color: #f2f2f2;
    position: absolute;
    bottom: 20px;
}

.card-author-img {
    height: 48px;
    width: 48px;
    margin-bottom: 5px;
}
</style>
