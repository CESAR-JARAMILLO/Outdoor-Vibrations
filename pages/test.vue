<template>
  <div>
    <Navbar />
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
import Navbar from '../components/Navbar'
export default {
  components: {
    Navbar
  }

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
  margin-top: 40px;
  /* height: 60vh; */
  justify-content: space-around;
  font-family: 'Montserrat', sans-serif;
}

.left-col {
    /* margin-top: 20px; */
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.btn-container {
    width: 60%;
    display: flex;
    justify-content: space-between;
    /* margin-top: 20px; */
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
    width: 90%;
    font-weight: 400;
    margin: 20px;
}

.btn {
    /* margin-right: 2.5rem; */
    /* margin-top: 1rem; */
    background: linear-gradient(180deg, #58B727, #40916C);
    color: #fff;
    width: 100px;
    height: 35px;
    border: none;
    border-radius: 5px;
    font-size: 15px;
}

.landing-image {
  /* margin-top: 20px; */
  height: 180px;
  /* width: 200px; */
  /* margin: auto; */
}

.vector {
  /* margin-left: 10px; */
  position: absolute;
  bottom: 0;
  left: 0;
  z-index: -1;
  /* width: 500px; */
  /* height: 200px; */
}
</style>
