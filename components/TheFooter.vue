<template>
  <div class="container">
    <div class="columns">
      <div class="nav-links">
        <ul>
          <li v-for="link in navLinks">{{ link }}</li>
        </ul>
      </div>
      <div class="sm-links">
        <ul>
          <li v-for="link in smLinks">{{ link }}</li>
        </ul>
      </div>
      <div class="contact">
        <p>
          Willetton Pavilion<br>
          Apsley Rd, Willetton<br>
          info@wbc.asn.au<br>
          PO Box 348, Willetton, 6955</p>
      </div>
    </div>
    <div class="copy">
      &copy;WBC 2023
    </div>
  </div>
</template>

<script setup>

const navLinks = [
  'Home',
  'Register',
  'Division Information',
  'About the Club',
  'Merchandise',
]
const smLinks = [
  'Facebook Public Page',
  'Senior FB Group',
  'Junior FB Group',
  'Tee-ball FB Group',
  'Baseball WA',
  'TBAWA',
]

</script>

<style scoped>
li {
  list-style: none;
}

.container {
  position: relative;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  /* background: black; */
  /* z-index: 1; */
}

.container::after {
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  content: '';
  background-image: url('../assets/roundel.png');
  filter: grayscale(1) opacity(0.05);
  background-size: 140%;
  background-position: 50% 50%;
  background-repeat: no-repeat;
}

.columns {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

.copy {
  padding: 2rem;
}
</style>