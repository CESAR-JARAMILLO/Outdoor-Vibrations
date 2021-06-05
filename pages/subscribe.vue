<template>
  <div>
    <Navbar/>
    <main>
        <div class="left">
          <div class="subscribe-card">
            <h2>Connect to our community</h2>
            <p>Get email updates from Outdoor Vibrations and stay up-to-date on all of our new posts. We’ll also let you know when we have any special deals.</p>
            <form action="">
                <input type="text" placeholder="name">
                <input type="email" placeholder="email">
                <button>Subscribe</button>
            </form>
          </div>
        </div>
        <div class="right">
        <img src="../assets/blogging.png" alt="">
        </div>
    </main>
    <img class="vector" src="../assets/vector.png" alt="">
    <!-- <TheFooter/> -->
</div>
</template>

<script>
import Navbar from '../components/Navbar'
export default {
    name: 'subscribe',
    components: {
        Navbar
    }
}
</script>