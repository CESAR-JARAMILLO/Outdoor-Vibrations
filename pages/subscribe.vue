<template>
  <div>
    <Navbar />
    <main>
      <div class="left">
        <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSdnyXS_3PzawZCiSd3jUh3r_Krq3KQTUuDAjyeB1KmfgHN1QA/viewform?embedded=true" width="640" height="673" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
      </div>
      <div class="right">
        <img class="main-image" src="../assets/blogging.png" alt="">
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

iframe {
  width: 100%;
  height: 600px;
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
