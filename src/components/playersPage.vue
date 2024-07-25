<template>
    <div class="players" id="players">
        <h2>Players</h2>
        <div class="player-list-container">
        <div class="player-list">
            <!-- Loop through players data -->
            <div
                v-for="(player, index) in players"
                :key="index"
                class="player-card"
                @click="showPlayerDetails(index)">
                <!-- Player Card Photo -->
                        <img :src="player.cardPhoto" :alt="`Photo of ${player.name}`" class="player-photo" />
                        <div class="player-info">
                            <h3>{{ player.name }}</h3>
                            <p>Number: {{ player.number }}</p>
                            <p>Position: {{ player.position }}</p>
                    </div>
            </div>
        </div>
    </div>
<!-- Modal for Player Details -->
        <div id="playerModal" class="modal">
            <div class="modal-content">
                <span class="close" @click="closeModal">&times;</span>
                <h2 id="playerName">{{ selectedPlayer.name }}</h2>
                <!-- Modal Photo -->
                <img id="playerPhoto" :src="selectedPlayer.modalPhoto" alt="Player Photo" class="modal-photo" />
                <p id="playerNumber">Number: {{ selectedPlayer.number }}</p>
                <p id="playerPosition">Position: {{ selectedPlayer.position }}</p>
                <p id="playerBio">{{ selectedPlayer.bio }}</p>
            </div>
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue'
    import img1 from '../assets/img/me1.jpg'
    import img2 from '../assets/img/me.jpg'
    import img3 from '../assets/img/jamy.jpg'
    import img4 from '../assets/img/jamy2.jpg'
    import img5 from '../assets/img/wolf.jpg'
    import img6 from '../assets/img/wolf2.jpg'
    import img7 from '../assets/img/karma2.jpg'
    import img8 from '../assets/img/karma.jpg'
    import img9 from '../assets/img/yoegi.jpg'
    import img10 from '../assets/img/yoegi2.jpg'
    import img11 from '../assets/img/jigme2.jpg'
    import img12 from '../assets/img/jigme.jpg'
    import img13 from '../assets/img/shyan.jpg'
    import img14 from '../assets/img/shyam.jpg'
    import img15 from '../assets/img/shek2.jpg'
    import img16 from '../assets/img/shek.jpg'
    import img17 from '../assets/img/xnmbauua.jpg'
    import img18 from '../assets/img/xnmbauua2.jpg'
    import img19 from '../assets/img/kingzang.jpg'
    import img20 from '../assets/img/ankara.jpg'
    import img21 from '../assets/img/das.jpg'
    import img22 from '../assets/img/das2.jpg'
    import img23 from '../assets/img/rangdel.jpg'
    import img24 from '../assets/img/rangdel2.jpg'
    import img25 from '../assets/img/chophel.jpg'
    import img26 from '../assets/img/chophel2.jpg'
    import img27 from '../assets/img/dazai.jpg'
    import img28 from '../assets/img/dazai2.jpg'
    import img29 from '../assets/img/boning.jpg'
    import img30 from '../assets/img/boning2.jpg'

        
  // Define players data with separate photos for card and modal
    const players = ref([
    {
        name: "Yeshi Dorji",
        number: 49,
        position: "Midfielder",
        cardPhoto: img1,  // Photo for card
        modalPhoto: img2,  // Photo for modal
        bio: "Yeshi is known for his goal-scoring ability and creativity."
    },
    {
        name: "Jamyang Dorji",
        number: 6,
        position: "Midfielder",
        cardPhoto: img3,
        modalPhoto: img4,
        bio: "Jamyang is known for his creativity and passing range."
    },
    {
        name: "Ugyen Wangchuk",
        number: 9,
        position: "Forward",
        cardPhoto: img5,
        modalPhoto: img6,
        bio: "Wolf is a forward known for his speed and agility."
    },
    {
        name: "Karma Tenzin",
        number: 17,
        position: "Forward",
        cardPhoto: img7,
        modalPhoto: img8,
        bio: "Karma is a versatile forward with a strong work ethic."
    },
    {
        name: "Yoegi Dwison Jumhadi",
        number: 7,
        position: "Forward",
        cardPhoto: img9,
        modalPhoto:img10,
        bio: "Yoegi is a dynamic forward with a knack for finding the net."
    },
    {
        name: "Jigme Kinzang",
        number: 11,
        position: "Midfielder",
        cardPhoto: img11,
        modalPhoto: img12,
        bio: "Jigme contributes to both defense and attack with equal skill."
    },
    {
        name: "Shyam Kumar Neopany",
        number: 21,
        position: "Defender",
        cardPhoto: img13,
        modalPhoto: img14,
        bio: "Shyam is a solid defender with excellent tackling skills."
    },
    {
        name: "Abishek Ghalley",
        number: 3,
        position: "Defender",
        cardPhoto: img15,
        modalPhoto: img16,
        bio: "Karba is known for his defending skills and leadership."
    },
    {
        name: "Sumpanna Acharya",
        number: 13,
        position: "Forward",
        cardPhoto: img17,
        modalPhoto: img18,
        bio: "Sumpanna brings speed and precision to the forward position."
    },
    {
        name: "Kuenzang Jamtsho",
        number: 10,
        position: "Forward",
        cardPhoto: img19,
        modalPhoto: img20,
        bio: "Kuenzang is an experienced dribbler with excellent game reading."
    },
    {
        name: "Dechen Dorji",
        number: 8,
        position: "Defender",
        cardPhoto: img21,
        modalPhoto: img22,
        bio: "Dechen is a strong defender with great positional awareness."
    },
    {
        name: "Choeing Rangdel",
        number: 30,
        position: "Midfielder",
        cardPhoto: img23,
        modalPhoto: img24,
        bio: "Rangdel excels in midfield control and passing."
    },
    {
        name: "Yeshi Chophel",
        number: 18,
        position: "Goal Keeper",
        cardPhoto: img25,
        modalPhoto: img26,
        bio: "Chophel is a reliable goalkeeper with great reflexes."
    },
    {
        name: "Tshering Dendup",
        number: 16,
        position: "Defender",
        cardPhoto: img27,
        modalPhoto:img28,
        bio: "Dazai provides solid defensive cover and support."
    },
    {
        name: "Sonam Tobgay",
        number: 23,
        position: "Defender",
        cardPhoto: img29,
        modalPhoto: img30,
        bio: "Sonam is a dependable defender with strong tactical understanding."
    }
])  
  // Ref to store selected player details
    const selectedPlayer = ref({})
  // Function to show player details in the modal
    const showPlayerDetails = (index) => {
        selectedPlayer.value = players.value[index]
        document.getElementById('playerModal').style.display = 'block'
}

  // Function to close the modal
    const closeModal = () => {
        document.getElementById('playerModal').style.display = 'none'
}

  // Close the modal when clicking outside of it
    window.onclick = function (event) {
    if (event.target === document.getElementById('playerModal')) {
        closeModal()
    }
}
</script>

<style scoped>

.players h2{
    text-align: center;
    font-size: 2rem;
    text-decoration: underline;
    color: white;
}
.player-list-container {
    overflow-x: auto;
    white-space: nowrap;
    padding: 10px 0;
    background-color: #000;
    border-radius: 10px;
}

/* Player List Flexbox */
.player-list {
    display: flex;
    flex-wrap: nowrap;
}

/* Individual Player Card */
.player-card {
    color: #000;
    font-size: 1rem;
    padding: 35px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-radius: 8px;
    background-color: #ffec00;
    backdrop-filter: blur(30px);
    margin: 10px;
    width: 400px;
    cursor: pointer;
    transition: transform 0.2s, box-shadow 0.2s;
}

/* Hover Effect for Player Cards */
.player-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

/* Player Photo */
.player-photo {
    width: 150px;
    height: 150px;
    border-radius:50%;
    margin-bottom: 40px;
    border: 4px solid black;
    padding: 2px;
}

/* Player Info Section */
.player-info {
    padding: 10px;
    text-align: left;
}

/* Player Info Heading */
.player-info h3 {
    margin: 5px 0;
    font-size: 1.2rem;
}

/* Player Info Paragraphs */
.player-info p {
    margin: 5px 0;
    font-size: 1rem;
}

/* Modal Styles */
.modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0, 0, 0, 0.7);
}   

/*Modal Content Box */
.modal-content {
    background-color: #1a1a1a;
    margin: 10% auto;
    padding: 20px;
    border: 2px solid #ffec00;
    width: 80%;
    max-width: 18rem;
    border-radius: 40px;
    text-align: center;
    color: #fff;
}

/* Modal Heading */
.modal-content h2 {
    margin-top: 0;
    color: #fff;
}

/* Modal Photo */
.modal-photo {
    width: 200px;
    height:300px;
    margin: 0.5rem;
    border: 2px solid #ffec00;
    border-radius: 30px;
}

/* Close Button */
.close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
}

/* Close Button Hover Effect */
.close:hover,
.close:focus {
    color: #fff;
    text-decoration: none;
    cursor: pointer;
}
@media(max-width: 768px) {
    .player-info h3 {
        font-size: 0.9rem;
    }
    .player-info p {
        font-size: 0.8rem;
    }
}
@media (max-width: 481px) {
    .player-card {
        width: 100%;
        max-width: 180px;
        max-height: 300px;
    }
}

</style>