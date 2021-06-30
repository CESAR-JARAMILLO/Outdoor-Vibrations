<template>
  <div>
    <!-- <Navbar /> -->
    <div class="main">
      <div class="left-col">
        <h1>Connecting to Nature</h1>
        <h2>Have a love for all things that are outdoors?</h2>
        <div class="btn-container">
          <NuxtLink to="subscribe">
            <button class="btn" href="">
              Join Now
            </button>
          </NuxtLink>
          <NuxtLink to="blogs">
            <button class="btn" href="">
              Read Blog
            </button>
          </NuxtLink>
        </div>
      </div>
      <div class="right-col">
        <img class="landing-image" src="../assets/landing-pic.png" alt="">
      </div>
    </div>
    <img class="vector" src="../assets/vector.png" alt="">
  </div>
</template>

<script>
export default {
}
</script>

<style scoped>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.main {
  display: flex;
  text-align: center;
  flex-direction: column-reverse;
  margin-top: 20px;
  justify-content: space-around;
  font-family: 'Montserrat', sans-serif;
}

.left-col {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.btn-container {
    width: 300px;
    display: flex;
    justify-content: space-between;
    margin-top: 12px;
}

h1 {
    font-size: 54px;
    width: 90%;
    color: #40916C;
    font-weight: 700;
    background: -webkit-linear-gradient(#40916C, #58B727);
    background-clip: initial;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-family: 'Montserrat', sans-serif;
}

h2 {
    font-size: 30px;
    width: 75%;
    font-weight: 400;
    margin: 20px;
}

.btn {
    background: linear-gradient(180deg, #58B727, #40916C);
    color: #fff;
    width: 140px;
    height: 60px;
    border: none;
    border-radius: 5px;
    font-size: 18px;
}

.landing-image {
  height: 180px;
}

.vector {
  position: absolute;
  bottom: 0;
  left: 0;
  z-index: -1;
}

@media (max-height: 720px) {
  .main {
    height: 720px;

  }

  .vector {
    margin-top: -80px;
    position: relative;
  }
}

@media (min-width: 780px) {
  .landing-image {
    height: 240px;
  }

  h2 {
    width: 50%;
  }

  .vector {
    height: 250px;
    width: 100vw;
  }
}

@media (min-width: 1024px) {
  .main {
    display: flex;
    flex-direction: row;
    text-align: left;
    height: 60vh;
    margin-top: 40px;
  }

  .left-col {
    align-items: center;
  }

  .right-col {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  h1 {
    font-size: 64px;
    width: 80%;
  }
  h2 {
    width: 80%;
  }

  .landing-image {
    height: 440px;
    margin-right: 20px;
  }

  .btn-container {
    width: 80%;
    justify-content: left;
  }

  .btn {
    margin-right: 22px;
    height: 70px;
    width: 200px;
    font-size: 24px;
  }
}
</style>
