<template>
    <section>
        <a href="#/"><img src="/src/assets/Logo.png" alt="logo crea" style="width: 100px"></a>
        <a href="#/devweb">DevWeb</a>
        <h1>Borne d'arcade créa design</h1>
        
        <div class="riddle">

            <!-- Couleurs -->

            <div class="riddle-content">
                <p>1/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><div class="color red"></div></a>
                    <a @click="RightAnswer()"><div class="color red-good"></div></a>
                    <a @click="WrongAnswer()"><div class="color red"></div></a>
                    <a @click="WrongAnswer()"><div class="color red"></div></a>
                </div>
                <p>Quelle est la bonne couleur ?</p>
            </div>
            <div class="riddle-content">
                <p>2/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><div class="color green"></div></a>
                    <a @click="WrongAnswer()"><div class="color green"></div></a>
                    <a @click="WrongAnswer()"><div class="color green"></div></a>
                    <a @click="RightAnswer()"><div class="color green-good"></div></a>
                </div>
                <p>Quelle est la bonne couleur ?</p>
            </div>
            <div class="riddle-content">
                <p>3/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><div class="color purple"></div></a>
                    <a @click="WrongAnswer()"><div class="color purple"></div></a>
                    <a @click="RightAnswer()"><div class="color purple-good"></div></a>
                    <a @click="WrongAnswer()"><div class="color purple"></div></a>
                </div>
                <p>Quelle est la bonne couleur ?</p>
            </div>
            <div class="riddle-content">
                <p>4/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><div class="color yellow"></div></a>
                    <a @click="WrongAnswer()"><div class="color yellow"></div></a>
                    <a @click="RightAnswer()"><div class="color yellow-good"></div></a>
                    <a @click="WrongAnswer()"><div class="color yellow"></div></a>
                </div>
                <p>Quelle est la bonne couleur ?</p>
            </div>

            <!-- Logos -->

            <div class="riddle-content">
                <p>5/15</p>
                <div class="color-contener">
                    <a @click="RightAnswer()"><div class="color blue-good"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                </div>
                <p>Quelle est la bonne couleur ?</p>
            </div>
            <div class="riddle-content">
                <p>6/15</p>
                <div class="color-contener">
                    <a @click="RightAnswer()"><div class="color blue-good"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                </div>
                <p>Quelle est le bon logo ?</p>
            </div>
            <div class="riddle-content">
                <p>7/15</p>
                <div class="color-contener">
                    <a @click="RightAnswer()"><div class="color blue-good"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                </div>
                <p>Quelle est le bon logo ?</p>
            </div>
            <div class="riddle-content">
                <p>8/15</p>
                <div class="color-contener">
                    <a @click="RightAnswer()"><div class="color blue-good"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                </div>
                <p>Quelle est le bon logo ?</p>
            </div>
            <div class="riddle-content">
                <p>9/15</p>
                <div class="color-contener">
                    <a @click="RightAnswer()"><div class="color blue-good"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                </div>
                <p>Quelle est le bon logo ?</p>
            </div>
            <div class="riddle-content">
                <p>10/15</p>
                <div class="color-contener">
                    <a @click="RightAnswer()"><div class="color blue-good"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                    <a @click="WrongAnswer()"><div class="color blue"></div></a>
                </div>
                <p>Quelle est le bon logo ?</p>
            </div>
        </div>

    </section>
</template>

<script lang="ts">
export default {
    name: 'CreaDesign',

    
    methods: {
        RightAnswer() {
            window.scrollBy(0, 600)
        },

        WrongAnswer() {
            window.scroll(0, 0)
        }
    },

    mounted() {
        //
    },
}
</script>

<style scoped>
    .riddle {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: auto;
        flex-direction: column;
        gap: 200px;
        margin: 100px;
    }
    
    .riddle-content {
        display: flex;
        align-items: center;
        width: 500px;
        height: 400px;
        border: 10px solid black;
        gap: 20px;
        padding: 20px;
        flex-direction: column;
    }

    .color-contener {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        width: 70%;
        height: 80%;
        gap: 20px;
    }

    .color {
        width: 90px;
        height: 90px;
        margin: 5px;
        border-radius: 100%;
    }

    .red-good {
        background-color: #E52421;
    }

    .red {
        background-color: #AF2329;
    }

    .green-good {
        background-color: #30A946;
    }

    .green {
        background-color: #258937;
    }

    .purple-good {
        background-color: #A24C97;
    }

    .purple {
        background-color: #7B317A;
    }

    .yellow-good {
        background-color: #BBB025;
    }

    .yellow {
        background-color: #E2D823;
    }

    .blue-good {
        background-color: #2D4899;
    }

    .blue {
        background-color: #25378C;
    }

</style>