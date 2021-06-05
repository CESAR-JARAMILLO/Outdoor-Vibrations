<template>
  <div>
      <Navbar />
      <div class="featured">
          <div class="featured-text">
              <p class="featured-category">Featured</p>
              <h2 class="featured-title">The outdoors, breaking down the walls and reconnecting.</h2>
              <p class="featured-date">May 12, 2021</p>
          </div>
          <div class="featured-image">

          </div>
      </div>
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
