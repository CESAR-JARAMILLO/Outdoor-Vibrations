<template>
  <div>
    <Navbar/>
    <main>
        <div class="left">
          <div class="about-card">
            <h3>Passion</h3>
            <h2>A journey of truth, with no destination.</h2>
            <img src="../assets/mountain.png" alt="">
            <p>Here at Outdoor Vibrations we believe that the road to growth should have no end. With many paths of improvement, inner growth and strength is achieved with every step.</p>
            <p>Whether your connection to nature is vibrant, or are looking to taking your first steps. Adventure is better with company.</p>
            <div class="buttons">
              <a class="button">
                <strong>Read Blog</strong>
              </a>
            </div>
          </div>
        </div>
        <div class="right">
        <img src="../assets/about-pic.png" alt="">
        </div>
    </main>
    <img class="vector" src="../assets/vector.png" alt="">
    <!-- <TheFooter/> -->
</div>
</template>

<script>
import Navbar from '../components/Navbar'
export default {
    name: 'about',
    components: {
        Navbar
    }
}
</script>