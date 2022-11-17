<template>
    <section id="digicode">
        <a id="comeback" href="#/"><img src="/src/assets/back-button_white.png" alt="logo crea" style="width: 50px"></a>
        <img id="music" src="/src/assets/orateur_white.png" alt="musique" @click="Onplay()">
        <audio id="audio" src="/src/assets/Rebecсa BAR Soundtrack OST Theme _ Cyberpunk_ Edgerunners.mp3"></audio>

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
            if (code !== null) {
                if (code.innerHTML.length >= 5) {
                    if (code.innerHTML == "12345") {
                        console.log("bravo -> video")
                    }
                    else {
                        code.innerHTML = ""
                    }
                }
                else {
                    code.innerHTML += chiffre
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

</style>






<!-- digicode -->
<!-- <script language="javascript">
 

var num="0";
var code=new Array(num,num,num,num,num,num,num,num);
var pos=0;

for (var f = 0; f < 8; f++) {
  code[f]="v";
}

c1=new Image(); c1.src="c1.gif"
c2=new Image(); c2.src="c2.gif"
c3=new Image(); c3.src="c3.gif"
c4=new Image(); c4.src="c4.gif"
c5=new Image(); c5.src="c5.gif"
c6=new Image(); c6.src="c6.gif"
c7=new Image(); c7.src="c7.gif"
c8=new Image(); c8.src="c8.gif"
c9=new Image(); c9.src="c9.gif"
c0=new Image(); c0.src="c0.gif"
cv=new Image(); cv.src="cv.gif"

function affiche(){
  document.images.a.src=eval("c"+code[0]+".src");
  document.images.b.src=eval("c"+code[1]+".src");
  document.images.c.src=eval("c"+code[2]+".src");
  document.images.d.src=eval("c"+code[3]+".src");
  document.images.e.src=eval("c"+code[4]+".src");
  document.images.f.src=eval("c"+code[5]+".src");
  document.images.g.src=eval("c"+code[6]+".src");
  document.images.h.src=eval("c"+code[7]+".src");
}
function nouveau(num) {
  if (pos<8) {
    for (var f = 1; f < 8; f++) {
      code[f-1]=code[f];
    }
    code[7]=eval(num);
    pos+=1;
  }
  affiche();
}
function ok() {
  password="";
  for (var f = 0; f < 8; f++) {
    if (code[f]!="v") {password+=code[f]};
  }
  var locate;
  locate = password + ".htm";
  this.location.href = locate;
}
function cancel() {
  for (var f = 0; f < 8; f++) {
    code[f]="v";
  }
  pos = 0;
  affiche();
}
</script>
  -->