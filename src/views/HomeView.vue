<script setup>
  import Gallery from '../components/Gallery.vue'

  // here we will call the db for images

</script>

<template>
  <main>
    <div class="background">
      <div class="grid">
        <div v-for="grid in Array.from({length:64},(_,k)=>k)"></div>
      </div>
      <h1 class="main-title">WildLife Photography</h1>
    </div>
    <Gallery />
  </main>
</template>

<style scoped>
  main {
    overflow: hidden;
  }

  .background {
    height: 100vh;
    
    background-image: url('../assets/images/cover.jpg');
    background-position: bottom;
    background-size: cover;

    filter: grayscale(20%);

    position: relative;
  }

  .main-title {
    position: absolute;
    bottom: 15%;
    left: 5%;
    font-size: clamp(1rem, 8vw, 5rem);
  }

  .main-title::after {
    display: block;

    content: '2025 - ©Vasja Škarabot';
    font-size: clamp(.875rem, 1vw, 1rem);
    color: var(--color-text);

    font-weight: 100;

    background-color: #101f29;
    mask: linear-gradient(to right, transparent, black, transparent);

    text-align: center;
  }

  .grid {
    position: absolute;
    z-index: 10;
    width: 100vw;
    height: 70vh;
    mask: linear-gradient(black, transparent);

    display: grid;
    grid-template-columns: repeat(8, 1fr);
    grid-template-rows: repeat(8, 1fr);
    gap: 1px;
  }

  .grid div {
    background-color: #101f29;
  }

</style>
