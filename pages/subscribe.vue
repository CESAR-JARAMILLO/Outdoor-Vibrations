<template>
  <div>
    <Navbar />
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
  </div>
</template>

<script>
import Navbar from '../components/Navbar'
export default {
  name: 'Subscribe',
  components: {
    Navbar
  }
}
</script>

<style scoped>
* {
  margin: 0;
  box-sizing: border-box;
}

main {
    margin-top: 40px;
    height: 70vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    font-family: 'Roboto', sans-serif;
}
.left {
  display: flex;
  justify-content: center;
  align-items: center;
}

.right {
    /* padding: 40px 0 40px 100px; */
    display: flex;
    justify-content: center;
    align-items: center;
}

.right img {
  height: 480px;
  /* width: 35rem; */
}

.subscribe-card {
  /* font-family: 'Roboto', sans-serif; */
  /* margin-top: 3rem; */
  /* margin-left: 2.5rem; */
  padding: 0 18px;
  height: 550px;
  width: 450px;
  border-radius: 10px;
  text-align: center;
  background-color: #40916C;
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}

.subscribe-card h2 {
    font-size: 44px;
    font-weight: 600;
}

.subscribe-card p {
    font-size: 20px;
    font-weight: 400;
}

.subscribe-card form {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    height: 200px;
    width: 300px;

}

form input {
    width: 300px;
    height: 50px;
    border-radius: 5px;
    border: none;
}

form button {
    height: 40px;
    width: 120px;
    border-radius: 5px;
    border: none;
    background-color:   #58b727;
    color: #fff;
}

.vector {
  position: absolute;
  bottom: 0rem;
  left: 0;
  z-index: -1;
  width: 100vw;
  height: 50vh;
  /* margin-bottom: 20px; */
}
</style>
