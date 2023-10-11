<template>
  <div class="hero-content">
    <div class="left-content">
      <p class="h2">Welcome to the</p>
      <h1 class="club">
        Willetton&nbsp;Baseball&nbsp;Club
      </h1>
      <h2>Home of the Wildcats</h2>
      <blockquote>"Yesterday's home runs don't win today's&nbsp;games."
        <footer>-Babe Ruth</footer>
      </blockquote>

      <h3>Baseball | Softball | Tee-ball</h3>
    </div>
    <div class="tile-parent">
      <TileVert
        v-for="(filename, i) in  filenames "
        class="tile-vert"
        :key="'url' + i"
        :filename="filename"
        :idx="i"
      >
      </TileVert>
    </div>
  </div>
</template>

<script setup>

const filenames = ref(['wbcDGradePremiers.jpg',
  'wscAGradePremiers.jpg',
  'wtcBravesCupU10.jpg'])

</script>

<style scoped>
.hero-content {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 10%;
}

.left-content {
  color: white;
  mix-blend-mode: difference;
  max-width: 30%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

blockquote {
  font-size: 3rem;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;

  /* color: var(--green); */
  color: black;
  padding: 0.125em 0.25em;
  background: linear-gradient(var(--gold), var(--gold));
  margin: 0;
}

footer {
  text-align: right;
  font-size: 1.5rem;
}

h1,
h2,
.h2 {
  padding: 0;
  margin: 0;
}

h3 {
  margin-top: 2rem;
}

h2 {
  margin-bottom: 2rem;
}

h2,
.h2 {
  font-size: larger;
  font-style: italic;
}

.club {
  font-weight: 900;
  font-style: normal;
  font-size: xx-large;
}


.left-content,
.right-content {
  flex: 0 0 50%;
}

.tile-parent {
  display: flex;
  flex-direction: row;
  justify-content: center;
  background: transparent;
  gap: 1rem;
}
</style>