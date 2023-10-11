<template>
  <div class="contact-container">
    <h2>
      Contact Us Today
    </h2>
    <p>Want to find out more? Drop down to Willetton Park for a chat or send us your inquiry
      below.</p>
    <form>
      <div class="form-row">
        <label for="name">Name</label>
        <input
          id="name"
          type="text"
        />
      </div>
      <div class="form-row">
        <label for="email">Email</label>
        <input
          id="email"
          type="text"
        />
      </div>
      <div class="form-row">
        <label for="message">Message</label>
        <textarea id="message"></textarea>
      </div>
      <div class="form-row">
        <button type="submit">Submit</button>
      </div>
    </form>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.contact-container {
  width: 40em;
  margin: auto;
}

form {
  width: 30em;
  margin: auto;
}

.form-row {
  padding: 1em;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.label {
  flex: 0 0 6rem;
}

input,
textarea {
  flex: 0 0 auto;
  padding: 0.5em;
  width: 24em;

}

textarea {
  height: 10em;
}

button {
  padding: 0.5rem 1rem;
  margin: 0 0 0 auto;
}
</style>