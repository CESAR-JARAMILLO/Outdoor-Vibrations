<template>
  <div>
    <!-- <Navbar /> -->
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
        <img class="main-image" src="../assets/blogging.png" alt="">
      </div>
    </main>
    <img class="vector" src="../assets/vector.png" alt="">
  </div>
</template>

<script>
export default {
  name: 'Subscribe'
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
  justify-content: space-around;
  font-family: 'Montserrat', sans-serif;
}

.left {
  align-items: center;
}

.subscribe-card {
  padding: 0 18px;
  height: 550px;
  width: 100%;
  border-radius: 10px;
  text-align: center;
  background-color: #40916C;
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  margin: auto;
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

.right {
  margin: auto;
}

.main-image {
  height: 180px;
}

.freebirdFormviewerViewFooterEmbeddedBackground {
  display: none !important;
}

@media (min-width: 520px) {
  .subscribe-card {
    width: 500px;
  }
}

@media (min-width: 780px) {
  .main-image {
    height: 260px;
  }

  .subscribe-card {
    width: 540px;
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

  .right {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 50%;
  }

  .main-image {
    height: 500px;
    margin-left: 20px;
  }

  .vector {
    position: absolute;
    bottom: 0;
    z-index: -1;
  }
}

</style>
