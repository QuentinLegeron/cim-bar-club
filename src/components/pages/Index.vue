<template>
    <section id="bar">
        <a class="devweb" href="#/devweb"></a>
        <a class="creadesign" href="#/creadesign"></a>
        <a class="ThreeD" href="#/3D"></a>
        <a class="digicode" href="#/digicode"></a>
        <a class="videogame" href="#/videogame"></a>
        <img id="music" src="/src/assets/orateur_white.png" alt="musique" @click="Onplay()">
        <audio id="audio" src="/src/assets/Rebecсa BAR Soundtrack OST Theme _ Cyberpunk_ Edgerunners.mp3"></audio>
    </section>
</template>

<script lang="ts">

export default {
    name: 'Index',

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

    #bar{
        height: 100vh;
        width: auto;
        background-image: url("/src/assets/SCENE.png");
        background-size: cover;
    }

    #music {
        position: fixed;
        z-index: 100;
        right: 20px;
        top: 20px;
        width: 40px;
    }

    .devweb{
        position: absolute;
        height: 51px;
        width: 69px;
        bottom: 129px;
        left: 157px;
        z-index: 100;
    }

    .creadesign{
        position: absolute;
        height: 104px;
        width: 83px;
        bottom: 151px;
        right: 174px;
        z-index: 100;
    }

    .ThreeD{
        position: absolute;
        height: 41px;
        width: 63px;
        bottom: 217px;
        right: 318px;
        z-index: 100;
    }

    .digicode{
        position: absolute;
        height: 51px;
        width: 40px;
        bottom: 283px;
        left: 288px;
        z-index: 100;
    }

    .videogame{
        position: absolute;
        height: 63px;
        width: 77px;
        bottom: 153px;
        right: 27px;
        z-index: 100;
    }

</style>