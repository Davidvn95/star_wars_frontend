<template>
    <section class="container" id="home">
        <div class="div-logo">
            <a href="/#characters">
                <img
                    src="https://www.freepnglogos.com/uploads/star-wars-logo-3.png"
                    alt=""
                    class="logo" />
            </a>
        </div>
        <img
            src="https://www.xtrafondos.com/wallpapers/resized/el-ascenso-de-skywalker-star-wars-10903.jpg?s=large"
            alt=""
            class="image" />
    </section>
</template>

<style scoped>
.container {
    position: relative;
    /* min-height: 100vh; */
}
.div-logo {
    position: absolute;
    width: 100%;
    height: 100%;
    display: grid;
    place-items: center;
}
.logo {
    width: 45rem;
    opacity: 100;
    cursor: pointer;
}
.image {
    margin-top: 3rem;
    height: 100vh;
}
</style>
