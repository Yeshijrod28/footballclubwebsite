<template>
    <div class="contact" id="contact">
        <h1>Contact Us</h1>
        <ul>
            <li><a href="https://www.instagram.com/dtudrukpasfc_official?igsh=MXIwMXdjenlkZnhxcQ=="><img src="../assets/img/instagram.png" style="width:2rem;" alt=""></a>dtudrukpasfc_official</li>
            <li><a href=""><img style="width:2rem;" src="../assets/img/gmail.png" alt=""></a>dtudrukpasfc@gmail.com</li>
            <li><a href=""><img style="width:2rem;" src="../assets/img/phone-call.png" alt=""></a>+91 9289718605</li>
            <li><a href=""><img style="width:2rem;" src="../assets/img/location.png" alt=""></a>Delhi Technological University</li>
        </ul>
    </div>
</template>

<style scoped>
.contact{
    text-align: center;
    background-color: #ffec00;
}
.contact ul{
    list-style: none;
    display: flex;
    margin: 1rem;
    justify-content: center;
}
.contact ul li{
    display: flex;
    flex-direction: column;
    margin: 0 2rem;
}
@media(max-width: 768px) {
    .contact ul {
        flex-direction: column;
        align-items: center;
    }
}
@media(max-width: 426px) {
    .contact{
        width: 107.5%;
    }
}
@media(max-width: 376px) {
    .contact{
        width: 108.5%;
    }
}
@media (max-width: 321px) {
    .contact{
        width: 110%;
    }
}
</style>