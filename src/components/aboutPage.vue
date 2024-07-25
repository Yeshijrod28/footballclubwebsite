<template>
    <div class="about" id="about">
    <h2>About Us</h2>
        <div class="about-container">
            <img src="../assets/img/about.jpg" alt="shardha vs dtu">
        <p>Welcome to the DTU Drukpas Football Club official page! Established in 2021, our team has been a cornerstone of pride and excellence. Over the years, we have cultivated a rich tradition of sportsmanship, teamwork, and competitive spirit. Our dedicated and talented players are committed to maintaining the highest standards on and off the field, fostering a culture of growth, discipline, and community engagement. Whether you're a student, alumni, or fan, we invite you to join us in celebrating the passion and spirit of DTU Drukpas football. Palden Drukpa Gyelo!! </p>
        </div>
    </div>
</template>

<style scoped>
.about{
    background-color: #1a1a1a;
}
.about h2{
    font-size: 2rem;
    text-align: center;
    text-decoration: underline;
    color: white;
    padding: 1rem;
}
.about-container{
    display: flex;
}
.about-container img{
    margin: 2rem;
    height: 40vh;
}
.about-container p{
    display: block;
    font-size: 1rem;
    margin: 2rem;
    padding: 1rem;
    color: white;
}
@media(max-width: 768px) { 
    .about-container {
        flex-direction: column;
        align-items: center;
    }
    .about-container p {
        font-size: 0.9rem;
}}
@media (max-width: 481px) {
    .about-container p {
        font-size: 0.8rem;
    }
}

</style>