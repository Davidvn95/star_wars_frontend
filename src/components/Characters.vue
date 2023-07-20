<script setup>
import { ref } from "vue";

const data = ref(null);
const error = ref(null);

fetch("http://34.125.25.44:8000/characters")
    .then((res) => {
        console.log(res);
        if (typeof res === 'object') {
            return res.json()
        }
        else throw new Error('La respuesta no es un JSON valido');
    })
    .then((json) => (data.value = json))
    .catch((err) => (error.value = err));
</script>

<template>
    <section class="characters" id="characters">
        <h1 class="titulo">Personajes</h1>
        <div v-if="error">Oops! Error encountered: {{ error.message }}</div>
        <div v-else-if="data" class="container">
            <div v-for="item in data.data" class="card">
                <span><strong>Nombre:</strong> {{ item.name }}</span>
                <span><strong>Genero:</strong> {{ item.gender }}</span>
                <span><strong>Estatura:</strong> {{ item.height }}</span>
                <span><strong>Año de nacimiento:</strong> {{ item.birth_year }}</span>
                <div class="content">
                    <span><strong>Peliculas en las que aparece:</strong></span>
                    <div><i v-for="film in item.films">{{ film.title }}, </i></div>
                </div>
            </div>
        </div>
        <div v-else>Loading...</div>
    </section>
</template>

<style scoped>
.characters {
    width: 100%;
    min-height: 100vh;
    background: rgb(2, 0, 36);
    background: linear-gradient(180deg, rgb(17 30 36) 0%, rgb(6 41 60) 100%);
    display: flex;
    flex-direction: column;
    padding: 2rem 0;
}

.titulo {
    color: #d98400;
}

.container {
    width: 100%;
    display: grid;
    grid-template-columns: repeat(3, auto);
    justify-content: center;
    align-items: center;
    gap: 1rem;
}
.card {
    display: flex;
    flex-direction: column;
    width: 20rem;
    height: 15rem;
    border: 1px solid white;
    border-radius: 1rem;
    align-items: flex-start;
    justify-content: space-around;
    padding: 0.7rem;
    /* gap: 0.5rem; */
}
.content {
    padding: 0;
    display: flex;
    flex-direction: column;
    width: 100%;
}
</style>
