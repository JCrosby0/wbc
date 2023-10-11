<template>
  <div class="page-layout">
    <section class="hero-image">
      <TileGrid></TileGrid>
    </section>
    <section class="white">
      <OurClub />
    </section>
    <section class="green">
      <FindUs></FindUs>
    </section>
    <section class="gold">
      <ContactForm />
      <GoogleMaps />
    </section>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.page-layout {
  position: relative;
  width: 800px;
  margin: auto;
  top: 0px;
  z-index: 1;
}

section {
  margin: auto;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.hero-image {
  position: relative;
  width: 1200px;
  height: 80vh;
  transform: translate(-200px);
}

.hero-image::before {
  content: '';
  height: 80vh;
  width: 200%;
  position: absolute;
  /* top: -120px; */
  left: -50%;
  background-image: url('../assets/willetton_diamond.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  filter: grayscale(1);
  mix-blend-mode: multiply;
}

.hero-image::after {
  content: '';
  height: 80vh;
  width: 200%;
  position: absolute;
  /* top: -120px; */
  left: -50%;
  background: var(--green);
  z-index: -1;
  mix-blend-mode: multiply;
}

.white {
  position: relative;
  height: 100vh;
}

.white::after {
  content: '';
  height: 100vh;
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background-image: url('../assets/roundel.png');
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
  filter: opacity(0.2);
  z-index: -1;
}

.green {
  background-image: url('../assets/chainFence.jpg');
  background-size: cover;
  background-position: center;
  position: relative;
  width: 300%;
  left: -100%;
}

.gold {
  position: relative;
  background-color: var(--gold);
  width: 300%;
  left: -100%;
}

.gold>* {
  flex: 0 0 50%;
}

.black {
  background-color: black;
}
</style>