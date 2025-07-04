<script setup>
  import Gallery from '@/components/Gallery.vue'

  // here we will call the db for images

</script>

<template>
  <main>
    <div class="background">

      <div class="grid">
        <div v-for="grid in Array.from({length:64},(_,k)=>k)"></div>
      </div>

      <div class="about">
        <p class="hello">Hello!</p>
        <p>
          Welcome to my wildlife project. 
          Here I will share my photography journey starting from today 04/07/2025. 
          I know the images won't look professional as I'm not willing to spend a bigger amount on money for a camera than a used Volkswagen Golf,
          but I still think it's a fun hobby I was always willing to try.
        </p>
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

    content: 'Copyright © 2025 — Vasja Škarabot';
    font-size: clamp(.875rem, 1vw, 1rem);
    color: var(--color-text);

    font-weight: 100;

    background-color: #101f29;
    border-radius: 2rem;

    text-align: center;
  }

  .grid {
    position: absolute;
    z-index: 10;
    width: 100%;
    height: 70vh;
    mask: linear-gradient(black, transparent);

    display: grid;
    grid-template-columns: repeat(8, 1fr);
    grid-template-rows: repeat(8, 1fr);
    gap: 1px;
  }

  .grid div {
    background-color: #6598ba;
  }

  .about {
    position: absolute;
    top: 1.85rem;
    right: 1rem;
    z-index: 10;

    max-width: 600px;
    color: var(--color-text);

    padding: 1rem;

    border-radius: 2rem 0 2rem 2rem;

    background: radial-gradient(circle at 0 0, #101f29d0, black);

    margin-left: 1rem;
  }

  .about p:not(.hello) {
    font-size: .875rem; 
    font-weight: 100; 
    line-height: 1.25rem;
  }

  .hello {
    font-weight: 600;
    color: white;
  }

  .hello::after {
    content: "";
    display: block;
    width: 100%;
    height: 1px;
    background-color: white;

    mask: linear-gradient(to left, black, transparent);
  }
</style>
