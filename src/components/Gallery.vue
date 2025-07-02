<template>
    <div class="container">
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
</template>

<style scoped>
    .container {
        min-height: 100vh;
        max-width: 100%;
        background-color: #0D1A22;
        background-image: 
            radial-gradient(circle at 10% 70%, #1E3A4C, transparent),
            radial-gradient(circle at 70% 10%, #000000, transparent 40%);
        
        display: flex;
        gap: 1rem;
    }

    .column {
        flex: 1;

        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    img {
        width: 100%;
        filter: grayscale(100%);
        transition: filter .5s linear;
    }

    img:hover {
        filter: grayscale(0);
        cursor: pointer;
    }

    
</style>