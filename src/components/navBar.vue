<template>
    <nav>
        <ul>
            <li><img src="../assets/img/Dtu drukpas.png" alt="DTU Drukpas FC Logo"></li>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#players">Players</a></li> 
            <li><a href="#gallery">Gallery</a></li>
            <li><a href="#matches">Matches</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</template>
<style scoped>
nav{
    position: fixed;
    background-color: #ffec00;
    width: 100%;
    z-index: 2000;
    opacity: 0.8;

}
nav ul{
    display: flex;
    list-style: none;
    position: sticky;
    height: 50px;
    width: 100%;
}
nav ul li{
    margin: 1rem;
}
nav ul li a{
    text-decoration: none;
    color: #000;
}
nav ul li a:active{
    font-size: 1.2rem;
    text-decoration: underline;
}
nav ul img{
    height: 100px;
    width: 100px;
    border-radius:50% ;
}
@media (max-width: 481px) {
    nav ul li{
        margin: 1rem 0.2rem;
        font-size: 0.7rem;
    }
}
@media (max-width: 321px) {
    nav ul li{
        margin: 1rem 0.1rem;
        font-size: 0.6rem;
    }
}
</style>