<template>
    <section id="jv">
        <a id="comeback" href="#/"><img src="/src/assets/back-button_white.png" alt="logo crea" style="width: 50px"></a>
        <img id="music" src="/src/assets/orateur_white.png" alt="musique" @click="Onplay()">
        <audio id="audio" src="/src/assets/Rebecсa BAR Soundtrack OST Theme _ Cyberpunk_ Edgerunners.mp3"></audio>

        <p class="message-green message1">Bravo tu as réparé la machine !</p>
        <p class="message-green message2">6</p>

        <p class="message-red start1">Dommage La machine est cassée!</p>
        <p class="message-red start2">Répare là en remettant les actions dans l'orde</p>

        <div class="validation-button">
            <input type="number">
            <button @click="Validation()">Confirmer</button>
        </div>

        <div class="game">
            <div class="game-content">
                <img src="/src/assets/perso_3.png" alt="personnage 3">
                <p>1. atterri</p>
            </div>
            <div class="game-content">
                <img src="/src/assets/perso_1.png" alt="personnage 1">
                <p>2. Chevalier</p>
            </div>
            <div class="game-content">
                <img src="/src/assets/perso_4.png" alt="personnage 4">
                <p>3. buche</p>
            </div>
            <div class="game-content">
                <img src="/src/assets/perso_6.png" alt="personnage 6">
                <p>4. attaque</p>
            </div>
            <div class="game-content">
                <img src="/src/assets/perso_8.png" alt="personnage 8">
                <p>5. sauver</p>
            </div>
            <div class="game-content">
                <img src="/src/assets/perso_5.png" alt="personnage 5">
                <p>6. gobelin</p>
            </div>
            <div class="game-content">
                <img src="/src/assets/perso_2.png" alt="personnage 2">
                <p>7. saute</p>
            </div>
            <div class="game-content">
                <img src="/src/assets/perso_7.png" alt="personnage 7">
                <p>8. récupérer clé</p>
            </div>
            <div class="game-content">
                <img src="/src/assets/perso_9.png" alt="personnage 9">
                <p>9. princesse</p>
            </div>
        </div>
        
    </section>
</template>

<script lang="ts">
export default {
    name: 'videogame',

    methods: {
        Onplay() {
            var audio = document.getElementById("audio")
            if (audio !== null) {
                if (audio.paused) {
                    audio.play()
                }
                else {
                    audio.pause()
                }
            }  
        },

        Validation() {
            var input = document.querySelector('input') as HTMLInputElement;
            var value = input.value;
            if (value == "273146859") {
                var message = document.querySelector('.message-green') as HTMLParagraphElement;
                message.style.display = "block";
                var message = document.querySelector('.message1') as HTMLParagraphElement;
                message.style.display = "block";
                var message = document.querySelector('.message2') as HTMLParagraphElement;
                message.style.display = "block";
                var message = document.querySelector('.message-red') as HTMLParagraphElement;
                message.style.display = "none";
                var message = document.querySelector('.start1') as HTMLParagraphElement;
                message.style.display = "none";
                var message = document.querySelector('.start2') as HTMLParagraphElement;
                message.style.display = "none";
                var button = document.querySelector('button') as HTMLButtonElement;
                button.style.display = "none";
                var input = document.querySelector('input') as HTMLInputElement;
                input.style.display = "none";
            } else {
                var message = document.querySelector('.message-red') as HTMLParagraphElement;
                message.style.display = "block";
                var message = document.querySelector('.start1') as HTMLParagraphElement;
                message.style.display = "block";
                var message = document.querySelector('.start2') as HTMLParagraphElement;
                message.style.display = "block";
                var message = document.querySelector('.message-green') as HTMLParagraphElement;
                message.style.display = "none";
                var message = document.querySelector('.message1') as HTMLParagraphElement;
                message.style.display = "none";
                var message = document.querySelector('.message2') as HTMLParagraphElement;
                message.style.display = "none";
            }
        }
    },
}
</script>

<style scoped>
    #jv{
        height: 100vh;
        width: auto;
        background-color: #282827;
    }

    #comeback {
        position: fixed;
        z-index: 100;
        top: 20px;
        left: 20px;
    }

    #music {
        position: fixed;
        z-index: 100;
        right: 20px;
        top: 20px;
        width: 40px;
    }

    .message-green {
        display: none;
        text-align: center;
        padding-top: 120px;
        font-size: 100px;
        color: #00FF00;
    }

    .message-red {
        text-align: center;
        padding-top: 20px;
        font-size: 20px;
        color: #FF0000;
    }

    .validation-button {
        text-align: center;
        padding-top: 20px;
    }

    .game {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 80%;
    }

    .game-content {
        display: flex;
        color: white;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 11%;
        height: 25%;
    }

    .game img {
        width: 100%;
        height: 100%;
        object-fit: contain;
    }
</style>