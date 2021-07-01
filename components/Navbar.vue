<template>
  <b-navbar :centered="centered" :shadow="shadow">
    <template #brand>
      <b-navbar-item class="brand" tag="router-link" :to="{ path: '/' }">
        Outdoor Vibrations
      </b-navbar-item>
    </template>
    <template #start>
      <nuxt-link to="/" class="nav-item navbar-item">
        Home
      </nuxt-link>
      <nuxt-link to="/about" class="nav-item navbar-item">
        About
      </nuxt-link>
      <nuxt-link to="/blogs" class="nav-item navbar-item">
        Blog
      </nuxt-link>
    </template>

    <template #end>
      <b-navbar-item tag="div">
        <nuxt-link to="/subscribe">
          <div class="buttons">
            <a class="button">
              <strong>Subscribe</strong>
            </a>
          </div>
        </nuxt-link>
      </b-navbar-item>
    </template>
  </b-navbar>
</template>

<script>
export default {
  name: 'Navbar',
  data () {
    return {
      centered: true,
      shadow: true
    }
  }
}
</script>

<style>
nav {
    padding: 0 3.5rem;
}

.nav-item {
    color: black;
}

.nav-item:hover {
  color: #58B727 !important;
}

.brand {
    font-size: 36px;
    font-weight: bold;
}

.brand:hover {
    color: #58B727 !important;
}

a {
    font-size: 18px;
    font-weight: 600;
}

.button {
    background-color:#40916c;
    /* background-color: #58b727; */
    color: #fff;
}

.button:hover {
  background-color: #58b727;
  color: #fff;
}
</style>
