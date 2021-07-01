<template>
  <div>
    <main>
      <div class="left">
        <div class="about-card">
          <!-- <h3>Passion</h3> -->
          <h2>A journey of truth, with no destination.</h2>
          <img src="../assets/mountain.png" alt="">
          <p>Here at Outdoor Vibrations we believe that the road to growth should have no end. With many paths of improvement, inner growth and strength is achieved with every step.</p>
          <p>Whether your connection to nature is vibrant, or are looking to taking your first steps. Adventure is better with company.</p>
          <Nuxt-Link class="button" to="blogs">
            <strong>Read Blog</strong>
          </Nuxt-Link>
        </div>
      </div>
      <div class="right">
        <img class="main-image" src="../assets/about-pic.png" alt="">
      </div>
    </main>
    <img class="vector" src="../assets/vector.png" alt="">
  </div>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

main {
  display: flex;
  text-align: center;
  flex-direction: column-reverse;
  margin-top: 20px;
  justify-content: flex-end;
  font-family: 'Montserrat', sans-serif;
}

.main-image {
  height: 180px;
  margin-bottom: 20px;
}

.left {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.about-card {
  padding: 0 18px;
  height: 70vh;
  width: 100%;
  border-radius: 10px;
  color: #40916C;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.about-card p {
  margin-top: 10px;
  padding: 0 16px;
  font-size: 14px;
  font-weight: 500;
  color: #1b4332;
  width: 380px;
}

.about-card h3 {
  font-size: 20px;
  font-weight: 500;
  color: #1b4332;
}

.about-card h2 {
  margin-top: 12px;
  margin-bottom: 12px;
  font-size: 32px;
  font-weight: 600;
  width: 320px;
}

.button {
    background: linear-gradient(180deg, #58B727, #40916C);
    color: #fff;
    width: 140px;
    height: 60px;
    border: none;
    border-radius: 5px;
    font-size: 18px;
    margin-top: 28px;
}

.button:hover {
  width: 160px;
  height: 60px;
}

.vector {
  margin-top: -180px;
}

@media (max-height: 720px) {
  main {
    height: 720px;

  }
}

@media (min-width: 780px) {
  .main-image {
    height: 240px;
  }

  .about-card h2 {
    width: 400px;
    font-size: 38px;
  }

  .about-card p {
    width: 460px;
    font-size: 16px;
  }

  .vector {
    height: 250px;
    width: 100vw;
  }
}

@media (min-width: 1024px) {
  main {
    display: flex;
    flex-direction: row;
    text-align: left;
    margin-top: 40px;
  }

  .left {
    align-items: center;
    width: 50%;
    text-align: center;
  }

  .about-card h2 {
    width: 480px;
    font-size: 44px;
  }

  .right {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 50%;
  }

  .vector {
    position: absolute;
    bottom: 0;
    z-index: -1;
  }

  .main-image {
    height: 420px;
    margin-right: 20px;
  }
}
</style>
