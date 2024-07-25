<template>
    <div class="matches" id="matches">
        <h2>Matches</h2>
        <ul>
            <li>DTU Drukpas FC 6 - 3 Amity University</li>
            <li>DTU Drukpas FC 4 - 5 Shardha University</li>
            <li>DTU Drukpas FC 7 - 5 Cambodian Students Team</li>
            <li>DTU Drukpas FC 2 - 4 DTU ISS</li>
            <li>DTU Drukpas FC 7 - 4 South Asian University</li>
        </ul>
    </div>
</template>

<style scoped>

.matches{
    margin:2rem 0;
    background-color: #000;
    color: white;
}
.matches h2{
    text-align: center;
    text-decoration: underline;
    font-size: 2rem;
    margin-bottom: 2rem;
}
.matches ul li{
    list-style-type: none;
    text-align: center;
    margin:1rem;
    padding: 1rem;

}
@media(max-width: 768px) {
    .matches h2 {
        font-size: 1.2rem;
    }
}
@media (max-width: 481px) {
    .matches ul li{
        text-align: left;
        font-size: 0.9rem;
    }
    .matches h2 {
        font-size: 1rem;
    }
}
@media (max-width:376px){ 
    .matches ul li{
        font-size: 0.65rem;
    }
}

</style>