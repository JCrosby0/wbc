<template>
  <div class="find-us-content">
    <h2>Keep up to date</h2>
    Check out our governing bodies for news and events;
    <div class="gov-bodies">
      <div class="gov-body">Baseball WA<br>
        <a href="baseballwa.com.au">baseballwa.com.au</a>
      </div>
      <div class="gov-body">Softball WA<br>
        <a href="wa.softball.org.au">wa.softball.org.au</a>
      </div>
      <div class="gov-body">Tee-Ball Association of WA<br>
        <a href="tbawa.org.au">tbawa.org.au</a>
      </div>
    </div>
    Check out our registration sites:
    <div class="reg-sites">
      <div class="reg-site">GameDay<br>
        <a
          href="https://membership.mygameday.app/regoform.cgi?aID=29217&pKey=bfb650b8fca348fa1afb154c5d2f1b4d&cID=279805&formID=109897">GameDay
          (Baseball)</a>
      </div>
      <div class="reg-site">Revolutionise<br>

        <a href="https://revolutionise.com.au/willettonbcwildcats/">Revolutionise (Softball)</a>
      </div>
      <div class="reg-site">GameDay<br>
        <a
          href="https://membership.mygameday.app/regoform.cgi?aID=29310&pKey=d8a893e52b785a51ac649b0158a4c4bf&cID=280967&formID=110554">GameDay
          (Tee-ball)</a>
      </div>
    </div>
    Follow our teams on GameChanger
    <div class="gc">Game Changer</div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.find-us-content,
a,
a:visited {
  color: white;
}

.find-us-content>* {
  margin: 1em;
}

.find-us-content {
  width: 800px;
  margin: auto;
  border: 3px grey solid;
  background: #404040b0;
  backdrop-filter: blur(10px);
  padding: 3rem;
}

.gov-bodies,
.reg-sites {
  display: flex;
  flex-direction: row;
}

.gov-body,
.reg-site {
  flex: 1 1 33%;
  padding: 1em;
  border: 1px black solid;
}
</style>