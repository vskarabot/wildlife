<script setup>
import Filter from '@/components/Filter.vue';
</script>

<template>
    <div class="container">
        <Filter />
        <div class="gallery">
            <div class="column">
                <img src="../assets/images/gallery/buck.jpg" alt="lion" loading="lazy">
                <img src="../assets/images/gallery/turtle.jpg" alt="lion" loading="lazy">
                <img src="../assets/images/gallery/hum.jpg" alt="lion" loading="lazy">
                <img src="../assets/images/gallery/lion.jpg" alt="lion" loading="lazy">
            </div>
            <div class="column">
                <img src="../assets/images/gallery/kingfi.jpg" alt="lion" loading="lazy">
                <img src="../assets/images/gallery/turtle.jpg" alt="lion" loading="lazy">
                <img src="../assets/images/gallery/fox.jpg" alt="lion" loading="lazy">
                <img src="../assets/images/gallery/hum.jpg" alt="lion" loading="lazy">
            </div>
            <div class="column">
                <img src="../assets/images/gallery/buck.jpg" alt="lion" loading="lazy">
                <img src="../assets/images/gallery/lion.jpg" alt="lion" loading="lazy">
                <img src="../assets/images/gallery/kingfi.jpg" alt="lion" loading="lazy">
                <img src="../assets/images/gallery/fox.jpg" alt="lion" loading="lazy">
            </div>
        </div>
    </div>
</template>

<style scoped>
    .container, .gallery, .column {
        display: flex;
        gap: 1rem;
    }

    .container {
        min-height: 100vh;
        max-width: 100%;
        background-color: #0D1A22;
        background-image: 
            radial-gradient(circle at 10% 70%, #1E3A4C, transparent),
            radial-gradient(circle at 70% 10%, #000000, transparent 40%);
        
        flex-direction: column;
    }

    .column {
        flex: 1;

        flex-direction: column;
    }

    img {
        width: 100%;
        filter: grayscale(0);
        transition: filter .5s linear;
    }

    img:hover {
        filter: grayscale(80%) brightness(60%);
        cursor: pointer;
    }

    
</style>