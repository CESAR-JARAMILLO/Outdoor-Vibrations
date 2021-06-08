<template>
  <div>
      <Navbar />
      <NuxtLink to="blog/my-first-blog">
          <div class="featured">
          <div class="featured-text">
              <p class="featured-category">Featured</p>
              <h2 class="featured-title">The outdoors, breaking down the walls and reconnecting.</h2>
              <p class="featured-date">May 12, 2021</p>
          </div>
          <div class="featured-image">

          </div>
      </div>
      </NuxtLink>
      <div class="blog-cards">
          <BlogCard />
          <BlogCard />
          <BlogCard />
          <BlogCard />
          <BlogCard />
          <BlogCard />
      </div>
  </div>
</template>

<script>
import Navbar from '../components/Navbar'
import BlogCard from '../components/BlogCard'
export default {
    name: 'blogs',
    components: {
        Navbar,
        BlogCard
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
</style>
