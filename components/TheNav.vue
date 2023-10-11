<template>
  <div id="nav-container">
    <div class="content logo"></div>
    <div class="content"></div>
    <div class="content"><span class="hamburger">=</span></div>
  </div>
</template>

<script setup lang="ts">

function handleScroll() {
  const nav = document.getElementById('nav-container')
  if (nav !== null) {
    if (document.body.scrollTop > document.body.clientHeight || document.documentElement.scrollTop > document.body.clientHeight) {
      nav.style.height = "60px";
      nav.style.backgroundColor = "var(--green)"
    } else {
      nav.style.height = "120px"
      nav.style.backgroundColor = 'var(--none)'
    }
  }
}

onMounted(() => {
  if (process.client) {
    window.addEventListener('scroll', handleScroll)
  }
})
onDeactivated(() => {
  if (process.client) {
    window.removeEventListener("scroll", handleScroll)
  }
})

</script>

<style scoped>
.content {
  margin: auto 0;
  padding: 1rem;

}

.logo {
  margin-left: 2rem;
  /* max-width: 25em; */
  height: 75%;
  aspect-ratio: 2.5;
  background-image: url('../assets/willetton_year1977.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

#nav-container {
  position: sticky;
  top: 0px;

  display: flex;
  flex-direction: row;
  justify-content: space-between;
  background-size: 100%;
  background-position: center top;
  transition: 0.3s;
  z-index: 2;
}
</style>