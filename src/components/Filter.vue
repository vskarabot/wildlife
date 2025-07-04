<script setup>
import { ref } from 'vue';

    const selectedAnimalClass = ref(0);

    const selectAnimalClass = (index) => {
        selectedAnimalClass.value = index;
    }
</script>

<template>
    <div class="row" >
        <div 
            v-for="(animal, index) in ['All', 'Birds', 'Mammals', 'Reptiles']" 
            @click="selectAnimalClass(index)" 
            :class=" selectedAnimalClass === index ? 'selected' : null"
        >
            {{ animal }}
        </div>
    </div>
</template>

<style scoped>
    .row {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 1rem;
        margin-top: 1rem;
    }
    .row div {
        padding: .25rem 1rem .25rem 1rem;
        border-radius: 1rem;
        background: #152b3a;
    }
    .row div:hover {
        cursor: pointer;
    }
    .selected {
        border: 1px solid white;
    }
</style>