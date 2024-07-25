<template>
    <div class="gallery" id="gallery">
        <h1>Gallery</h1>
        <div class="image-container">  <img src="../assets/img/item2.jpg" alt="cambodia vs Dtu drukpas">
            <img src="../assets/img/item3.jpg" alt="">
            <img src="../assets/img/item4.jpg" alt="">
        </div>

        <div class="image-container2">
            <img src="../assets/img/item5.jpg" alt="">
            <img src="../assets/img/item6.jpg" alt="">
        </div>
        <video width="640" height="360" autoplay muted loop controls poster="../assets/img/bg.jpg">
            <source src="../assets/img/item1.mp4" type="video/mp4">
            <source src="../assets/img/item1.ogg" type="video/ogg">
            <source src="../assets/img/item1.webm" type="video/webm">
            Your browser does not support the video tag.
        </video>

    </div>
</template>

<style scoped>
.gallery{
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #1a1a1a;
}
.gallery h1{
    text-align: center;
    font-size: 2rem;
    text-decoration: underline;
    color: #fff;
}
.gallery img{
    height: 50vh;
    border: 4px solid #ffec00;
    border-radius: 30px;
}
.gallery video{
    border: 4px solid #ffec00;
    border-radius: 30px;
}
.gallery .image-container img{
    margin: 1rem;;
}
.gallery .image-container2{
    display: flex;
}
.gallery .image-container2 img{
    width: 45%;
    margin: 1rem;
}
@media(max-width: 768px) {
    .hero {
        height: 80vh;
    }
    .hero .heading {
        top: 60%;
        width: 80%;
        max-width: 300px;
    }

    .hero .heading h1 {
        font-size: 1.5rem;
    }
    .hero .heading p {
        font-size: 1rem;
    }

    .about-container {
        flex-direction: column;
        align-items: center;
    }
    .about-container p {
        font-size: 0.9rem;
    }
    .player-info h3 {
        font-size: 0.9rem;
    }
    .player-info p {
        font-size: 0.8rem;
    }
    .matches h2 {
        font-size: 1.2rem;
    }

    .gallery h1 {
        font-size: 1.2rem;
    }
    .contact ul {
        flex-direction: column;
        align-items: center;
    }
}
@media (max-width: 481px) {
    .gallery{
        width: 107.5%;
    }
    .gallery h1 {
        font-size: 1rem;
    }

    .gallery img,
    .gallery video {
        width: 100%;
        max-width: 380px;
    }
    .gallery .image-container2{
        flex-direction: column;
    }
    .gallery .image-container2 img {
        width: 100%;
        max-width: 380px;
    }
}
@media (max-width: 376px) {
    .gallery{
        width: 108.5%;
    }
}
@media (max-width: 376px) {
    .gallery img{
        width: 90%;
    }
    .gallery .image-container2 img{
        width: 90%;
    }
    .gallery video{
        width: 90%;
    }
}
@media (max-width: 321px) {
    .gallery{
        width: 110%;
    }
}
</style>