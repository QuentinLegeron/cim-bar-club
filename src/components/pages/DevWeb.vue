<template>
    <section id="devweb">
        <div class="big-image">
            <img src="/src/assets/interface_dev.png" alt="background">
        </div>
        <a id="comeback" href="#/"><img src="/src/assets/back-button_white.png" alt="logo crea" style="width: 50px"></a>
        <img id="music" src="/src/assets/orateur_white.png" alt="musique" @click="Onplay()">
        <audio id="audio" src="/src/assets/Rebecсa BAR Soundtrack OST Theme _ Cyberpunk_ Edgerunners.mp3"></audio>
        <div class="button-contener">
            <button class="button" @click="MyFunction()">Click pour rentrer la réponse</button>
        </div>
    </section>
</template>

<script lang="ts">

export default {
    name: 'DevWeb',

    methods: {
        ConsoleLogEnigma(answer: string | null) {
            const reponse = 'code'
            if (answer === reponse) {
                console.log("\n \n \n \nBien joué !\n \n La clef de l'axe dev web est un 4 noir.\n \n N'oublie pas de le noter pour pas l'oublier.\n Et de refermer la console en appuyant de nouveau sur F12\n \n \n \n")
                return
            }
            console.log("\n \n \n \nC'est un civil à respecter.\n Souvent gardien de nos entrées.\n Sur la route, il est suivi.\n En génétique, il nous définit.\n Qui est-il ?\n \n \n \n")
            if (answer === null) {
                console.log("\n \n \nEntre une reponse en appuyant sur le bouton pour avoir la clef de l'axe dev \n \n \n")
            }
            else{
                console.log('\n \n \n \nIndice :\n En informatique , il bug au moindre problème.\n il ne mesure que 4 lettres et commence par un C.\n \n \n \n')
            }
        },

        MyFunction() {
        let answer = prompt("Quelle est la réponse à l'énigme?", '')
        this.ConsoleLogEnigma(answer)
        },

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
    },

    mounted() {
        this.ConsoleLogEnigma(null)
    },
}

</script>

<style scoped>
    
    #devweb{
        height: 100vh;
        width: auto;
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

    .big-image {
        position: fixed;
        top: 0;
        left: 0;
        z-index: -10;
        height: 100vh;
    }

    .big-image img {
        height: auto;
        width: 100%;
        object-fit: cover;
    }

    .button-contener{
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
    }

    .button {
        color: black;
        font-size: larger;
        font-weight: 700;
        background-color: white;
        padding: 15px;
        border-radius: 20px;
    }

</style>