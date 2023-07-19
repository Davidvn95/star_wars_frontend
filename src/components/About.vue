<template>
    <section class="about" id="about">
        <h1 class="title">Sobre esta web</h1>
        <p class="text">
            Hola, soy David Vergara, Fullstack developer de Colombia y tengo 28 años. 
            Esta aplicación fué creada con el fin de mostrar el resultado del Upskilling de la
            academia <strong>Soy Henry</strong>.<br />
            <br />Upskilling es una capacitación que reciben los gradados para potenciar sus
            habilidades como full stack developer, en esta ocación aprendimos a desarrollar
            API's aplicando la arquitectura de microservicios, buenas prácticas en la
            estructura de archivos, manejo eficiente de errores, entre otros tips y
            conocimientos más. <br /><br />la API se encuentra desarrollada con Express,
            MongoDB y Mongoose, se encuentra contenida en docker y deployada en una VM de Google
            cloud. Tine el funcionamiento de un CRUD completo aunque inicialmente en
            esta web, solo se puede visualizar la respuesta.
            <br>
            <br>
            Esta web se encuentra desarrollada con Vue.js y deployada en vercel.
            <br>
            <br>
            Si quieres saber  más de mi visitame en:
            <ul class="list">
                <li><a href="https://www.linkedin.com/in/david-de-jes%C3%BAs-vergara-navarro-62169225a/" target="_blank">Linkedin</a></li>
                <li><a href="https://github.com/Davidvn95" target="_blank">GitHub</a></li>
                <li><a href="mailto:davidvergaraok@gmail.com">davidvergaraok@gmail.com</a></li>
            </ul>
        </p>
    </section>
</template>

<style scoped>
.about {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    background-color: rgb(6 41 60);
    align-items: center;
}

.title {
    color: #d98400;
}
.text {
    max-width: 60%;
    text-align: justify;
    text-justify: inter-word;
}
.list{
    width: 60%;
    text-align: left;
    margin: 0;
}
</style>
