<template>
    <section id="monkey">
        <a id="comeback" href="#/"><img src="/src/assets/back-button_white.png" alt="logo crea" style="width: 50px"></a>
        <img id="music" src="/src/assets/orateur_white.png" alt="musique" @click="Onplay()">
        <audio id="audio" src="/src/assets/Rebecсa BAR Soundtrack OST Theme _ Cyberpunk_ Edgerunners.mp3"></audio>
    </section>
</template>

<script lang="ts">
export default {
    name: '3D',

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
        }
    },
}
</script>

<style scoped>
    #monkey{
        height: 100vh;
        width: auto;
        background-image: url("/src/assets/suzanne.png");
        background-size: cover;
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
</style>