<template>
<div>
  <!-- <Navbar/> -->
  <main>
        <div class="left-col">
            <h1>Connecting to Nature</h1>
            <h2>Have a love for all things that are outdoors?</h2>
            <div class="btn-container">
                <NuxtLink to="subscribe"><button class="btn" href="">Join Now</button></NuxtLink>
                <NuxtLink to="blogs"><button class="btn" href="">Read Blog</button></NuxtLink>
            </div>
        </div>
        <div class="right-col">
            <img src="../assets/landing-pic.png" alt="">
        </div>
    </main>
    <img class="vector" src="../assets/vector.png" alt="">
<!-- <TheFooter/> -->
</div>

</template>

<script>
// import Navbar from '../components/Navbar'
// import TheFooter from '../components/TheFooter'

export default {
  components: {
    // Navbar,
    // TheFooter
  }
}
</script>