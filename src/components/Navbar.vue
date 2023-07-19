<template>
    <header class="nav">
        <a href="/#home">
            <span>Inicio</span>
        </a>
        <a href="/#characters">
            <span>Personajes</span>
        </a>
        <a href="/#about">
            <span>Acerca de</span>
        </a>
    </header>
</template>

<style scoped>
.nav {
    position: sticky;
    top: 0;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    max-width: 100%;
    height: 3rem;
    z-index: 100;
    background: linear-gradient(
        180deg,
        rgba(107, 62, 0, 0.55) 0%,
        rgba(185, 136, 0, 0.55) 100%
    );
    backdrop-filter: blur(0.5rem);
    padding: 0 1rem 0 1rem;
    margin-bottom: -5rem;
    font-size: x-large;
}
</style>
