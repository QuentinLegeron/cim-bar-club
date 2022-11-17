<template>
    <section id="digicode">
        <a id="comeback" href="#/"><img src="/src/assets/back-button_white.png" alt="logo crea" style="width: 50px"></a>
        <img id="music" src="/src/assets/orateur_white.png" alt="musique" @click="Onplay()">
        <audio id="audio" src="/src/assets/Rebecсa BAR Soundtrack OST Theme _ Cyberpunk_ Edgerunners.mp3"></audio>

        <div id="boxvideo"></div>

        <div>
            <p id="code"></p>
        </div>

        <div>
            <p @click="NewNumber(0)" class="number zero"></p>
            <p @click="NewNumber(1)" class="number one"></p>
            <p @click="NewNumber(2)" class="number two"></p>
            <p @click="NewNumber(3)" class="number three"></p>
            <p @click="NewNumber(4)" class="number for"></p>
            <p @click="NewNumber(5)" class="number five"></p>
            <p @click="NewNumber(6)" class="number six"></p>
            <p @click="NewNumber(7)" class="number seven"></p>
            <p @click="NewNumber(8)" class="number height"></p>
            <p @click="NewNumber(9)" class="number nine"></p>
        </div>
    </section>
</template>

<script lang="ts">
export default {
    name: 'digicode',

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

        NewNumber(chiffre: number) {
            var code = document.getElementById("code")
            var digicode = document.getElementById("digicode")
            if (code !== null) {
                if (code.innerHTML.length <= 4) {
                    code.innerHTML += chiffre
                    if (digicode !== null) {
                        digicode.style.backgroundImage = "url('/src/assets/digicode.png')"
                    }
                }
                if (code.innerHTML.length == 5) {
                    if (code.innerHTML == "45268") {
                        code.innerHTML = ""
                        const video = document.createElement('video')

                        // 👇️ Remote file
                        video.src = '/src/assets/animation_fin.mp4'

                        video.autoplay = true;
                        video.controls = true;
                        video.muted = false;
                        video.width = 1536;
                        video.height = 721;

                        const boxvideo = document.getElementById('boxvideo')
                        
                        if (boxvideo !== null) {
                            boxvideo.appendChild(video)
                        }
                    }
                    else {
                        if (digicode !== null) {
                            digicode.style.backgroundImage = "url('/src/assets/digicode_lueur_rouge.png')"
                        }
                        code.innerHTML = ""
                    }
                }
            }
        },
    },
}
</script>

<style scoped>
    #digicode{
        height: 100vh;
        width: auto;
        background-image: url("/src/assets/digicode.png");
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
    
    #code {
        position: fixed;
        text-align: left;
        width: 308px;
        z-index: 1;
        top: 220px;
        left: 753px;
        transform: translate(-50%, -50%);
        color: rgb(249, 249, 249);
        font-size: 65px;
        letter-spacing: 26px;
    }
    .number:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
    }

    .zero{
        position: fixed;
        z-index: 10;
        bottom: 147px;
        left: 701px;
        width: 80px;
        height: 55px;
        border-radius: 10px;
    }
    .one{
        position: fixed;
        z-index: 10;
        top: 320px;
        left: 611px;
        width: 80px;
        height: 55px;
        border-radius: 10px;
    }

    .two{
        position: fixed;
        z-index: 10;
        top: 320px;
        left: 701px;
        width: 80px;
        height: 55px;
        border-radius: 10px;
    }

    .three{
        position: fixed;
        z-index: 10;
        top: 320px;
        left: 791px;
        width: 80px;
        height: 55px;
        border-radius: 10px;
    }

    .for{
        position: fixed;
        z-index: 10;
        top: 387px;
        left: 610px;
        width: 80px;
        height: 55px;
        border-radius: 10px;
    }

    .five{
        position: fixed;
        z-index: 10;
        top: 387px;
        left: 701px;
        width: 80px;
        height: 55px;
        border-radius: 10px;
    }

    .six{
        position: fixed;
        z-index: 10;
        top: 387px;
        left: 791px;
        width: 80px;
        height: 55px;
        border-radius: 10px;
    }

    .seven{
        position: fixed;
        z-index: 10;
        top: 454px;
        left: 610px;
        width: 80px;
        height: 55px;
        border-radius: 10px;
    }

    .height{
        position: fixed;
        z-index: 10;
        top: 454px;
        left: 701px;
        width: 80px;
        height: 55px;
        border-radius: 10px;
    }

    .nine{
        position: fixed;
        z-index: 10;
        top: 454px;
        left: 791px;
        width: 80px;
        height: 55px;
        border-radius: 10px;
    }

    video {
        position: fixed;
        z-index: 100;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

</style>