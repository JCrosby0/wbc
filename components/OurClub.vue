<template>
  <div class="our-club-container">
    <div class="left">
      <DivisionCard
        class="div-bb"
        filename="baseballBattingUpright.jpg"
      >
        <template v-slot:division>Baseball</template>
        <template v-slot:ages>Ages 7 - Adult</template>
      </DivisionCard>
      <DivisionCard
        class="div-sb"
        filename="softballPitchingUpright.jpg"
      >
        <template v-slot:division>Softball</template>
        <template v-slot:ages>Ages 9 - Adult</template>
      </DivisionCard>
      <DivisionCard
        class="div-tb"
        filename="teeballBattingUpright.jpg"
      >
        <template v-slot:division>Tee-ball</template>
        <template v-slot:ages>Ages 4 - 11</template>
      </DivisionCard>
    </div>
    <div class="right">

      <h2>Our Club</h2>
      <p>
        The Willetton Baseball Club (Inc) is a multi-diamond sports club, comprising Tee-Ball, Baseball and Softball.</p>
      <p>
        Known as the <span class="highlight">“WBC Wildcats“</span>, we are one of the state's largest diamond sports
        clubs, catering from ages 4 and
        beyond.</p>
      <p>
        Founded in 1977, the club prides itself on providing a family friendly environment with a huge focus on junior
        development, as well as catering for the social or the serious diamond sport player of any age.
      </p>
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.our-club-container {
  display: flex;
  flex-direction: row;
}

.highlight {
  color: var(--green);
  font-weight: 900;
  font-size: larger;
}

.right {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 2rem;
}

.left {
  display: grid;
  grid-template-rows: 4fr;
  grid-template-columns: 2fr;
}

.div-bb {
  grid-row: 1/3;
  grid-column: 2/3;
}

.div-sb {
  grid-row: 2/4;
}

.div-tb {
  grid-row: 3/5;
}
</style>