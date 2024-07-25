<template>
    <div class="hero" id="home">
        <div class="heading">           
            <h1>The DRUKPAS</h1>
            <p>Just play. Have fun. Enjoy the game.</p>
        </div>
    </div>
    <hr style="height: 1rem;">
</template>

<style scoped>

.hero{
    background: url('../assets/img/bg.jpg');
    background-size: cover;
    height: 120vh;
    width: auto;
    margin-bottom: 0;
}
.hero .heading {
    position: absolute;
    left: 50%;
    top: 100%;
    transform: translateY(-50%);
    background-color: #ffec00;
    opacity: 0.7;
    text-align: center;
    padding: 20px;
}
.hero .heading h1{
    font-size: 3rem;
    color: black;
}
.hero .heading p{
    color: black;
    font-size: 2rem;
}
@media(max-width: 811px) {
    .hero {
        height: 60vh;
    }
    .hero .heading {
        top: 50%;
        width: 80%;
        max-width: 300px;
    }

    .hero .heading h1 {
        font-size: 1.5rem;
    }
    .hero .heading p {
        font-size: 1rem;
    }
}
@media (max-width: 481px) {
    .hero{
        height: 50vh;
        margin-right: -2rem;
        margin-left: -4.5rem;
    }
    .hero .heading{
        top: 40%;
        max-width: 200px;
        padding: 0.1rem;
    }
    .hero .heading h1 {
        font-size: 1.2rem;
    }

    .hero .heading p {
        font-size: 0.8rem;
    }
}
@media (max-width:376px){ 
    .hero .heading{
        max-width: 200px;
    }
}
@media (max-width:321px){ 
    .hero .heading{
        top: 35%;
        max-width: 160px;
    }
    .hero{
        height: 45vh;
        margin-right: -2rem;
    }
}
</style>