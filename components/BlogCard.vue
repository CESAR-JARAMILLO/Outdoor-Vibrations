<template>
  <div class="card">
    <div class="card-image">
        <figure class="image is-4by3">
            <img src="../assets/autumn.png" alt="Placeholder image">
        </figure>
    </div>
    <div class="card-content">
        <div class="media">
            <div class="media-content">
                <p class="card-category title is-6">Category</p>
            </div>
        </div>
            <div class="content">
                <p class="card-title title is-4">This is where the title goes</p>
                <time class="card-date" datetime="2016-1-1">Jan 1, 2016</time>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'BlogCard'
}
</script>

<style scoped>
.card-content {
    background-color: #1b4332;
    font-family: 'Roboto', sans-serif;
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
}

.card-author-img {
    height: 48px;
    width: 48px;
    margin-bottom: 5px;
}
</style>
