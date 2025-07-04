<script setup>
import Filter from '@/components/Filter.vue';

    const url = '/src/assets/images/gallery/';
    const images = [
        { name: 'Buck', url: 'buck.jpg' }, 
        { name: 'Kingfisher', url: 'kingfi.jpg' }, 
        { name: 'Lion', url: 'lion.jpg' }, 
        { name: 'Fox', url: 'fox.jpg' }, 
        { name: 'Hummingbird', url: 'hum.jpg' }, 
        { name: 'Turtle', url: 'turtle.jpg' },
    ];

</script>

<template>
    <div class="container">
        <Filter />
        <div class="gallery">
            <div class="imageContainer" v-for="image in images">
                <img :src="url + image.url" :key="image">
                <div class="imageInfo">
                    {{ image.name }}
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .container {
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

    .gallery {
        column-count: 1;
        column-gap: 1rem;
    }

    @media screen and (min-width: 600px) {
        .gallery {
            column-count: 2;
        }
    }

    @media screen and (min-width: 1024px) {
        .gallery {
            column-count: 3;
        }
    }

    .imageContainer {
        margin-bottom: 1rem;
        position: relative;
    }

    img {
        display: block;
        width: 100%;
        transition: filter .5s linear;
    }

    .imageContainer:hover {
        cursor: pointer;
    }

    .imageContainer:hover img {
        filter: brightness(50%);
    }

    .imageInfo {
        position: absolute;
        inset: 0 0 0 0;
        display: grid;
        place-items: center;

        color: white;
        font-size: 1.25rem;

        opacity: 0;
        transition: opacity .5s linear;
    }

    .imageInfo:hover {
        opacity: 1;
    }
    
</style>