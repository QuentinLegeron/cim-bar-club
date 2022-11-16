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
            
            <!-- Logos -->
            
            <div class="riddle-content">
                <p>6/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><img src="/src/assets/LOGO_COCA_COLA_Plan_de_travail_1.png" alt="coca 1" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/LOGO_COCA_COLA-03.png" alt="coca 3" class="logo-riddle"></a>
                    <a @click="RightAnswer()"><img src="/src/assets/LOGO_COCA_COLA-02.png" alt="coca 2" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/LOGO_COCA_COLA-04.png" alt="coca 4" class="logo-riddle"></a>
                </div>
                <p>Quelle est le bon logo ?</p>
            </div>
            <div class="riddle-content">
                <p>7/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><img src="/src/assets/CHUPACHUPS_Plan_de_travail_1.png" alt="chupa 1" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/CHUPACHUPS-03.png" alt="chupa 3" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/CHUPACHUPS-04.png" alt="chupa 4" class="logo-riddle"></a>
                    <a @click="RightAnswer()"><img src="/src/assets/CHUPACHUPS-02.png" alt="chupa 2" class="logo-riddle"></a>
                </div>
                <p>Quelle est le bon logo ?</p>
            </div>
            <div class="riddle-content">
                <p>8/15</p>
                <div class="color-contener">
                    <a @click="RightAnswer()"><img src="/src/assets/pepsi_logo-02.png" alt="pepsi 2" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/pepsi_logo_Plan_de_travail_1.png" alt="pepsi 1" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/pepsi_logo-03.png" alt="pepsi 3" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/pepsi_logo-04.png" alt="pepsi 4" class="logo-riddle"></a>
                </div>
                <p>Quelle est le bon logo ?</p>
            </div>
            <div class="riddle-content">
                <p>9/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><img src="/src/assets/pringles_Plan_de_travail_1.png" alt="pringles 1" class="logo-riddle"></a>
                    <a @click="RightAnswer()"><img src="/src/assets/pringles-02.png" alt="pringles 2" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/pringles-03.png" alt="pringles 3" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/pringles-04.png" alt="pringles 4" class="logo-riddle"></a>
                </div>
                <p>Quelle est le bon logo ?</p>
            </div>
            <div class="riddle-content">
                <p>10/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><img src="/src/assets/redbull_Plan_de_travail_1.png" alt="redbull 1" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/redbull-03.png" alt="redbull 3" class="logo-riddle"></a>
                    <a @click="RightAnswer()"><img src="/src/assets/redbull-02.png" alt="redbull 2" class="logo-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/redbull-04.png" alt="redbull 4" class="logo-riddle"></a>
                </div>
                <p>Quelle est le bon logo ?</p>
            </div>

            <!-- Ui-UX -->

            <div class="riddle-content">
                <p>11/15</p>
                <div class="color-contener">
                    <a @click="RightAnswer()"><img src="/src/assets/1.png" alt="interface ui-ux" class="ui-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/2.png" alt="interface ui-ux" class="ui-riddle"></a>
                </div>
                <p>Quelle est la bonne interface ui ?</p>
            </div>
            <div class="riddle-content">
                <p>12/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><img src="/src/assets/4.png" alt="interface ui-ux" class="ui-riddle"></a>
                    <a @click="RightAnswer()"><img src="/src/assets/3.png" alt="interface ui-ux" class="ui-riddle"></a>
                </div>
                <p>Quelle est la bonne interface ui ?</p>
            </div>
            <div class="riddle-content">
                <p>13/15</p>
                <div class="color-contener">
                    <a @click="RightAnswer()"><img src="/src/assets/5.png" alt="interface ui-ux" class="ui-riddle"></a>
                    <a @click="WrongAnswer()"><img src="/src/assets/6.png" alt="interface ui-ux" class="ui-riddle"></a>
                </div>
                <p>Quelle est la bonne interface ui ?</p>
            </div>
            <div class="riddle-content">
                <p>14/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><img src="/src/assets/8.png" alt="interface ui-ux" class="ui-riddle"></a>
                    <a @click="RightAnswer()"><img src="/src/assets/7.png" alt="interface ui-ux" class="ui-riddle"></a>
                </div>
                <p>Quelle est la bonne interface ui ?</p>
            </div>
            <div class="riddle-content">
                <p>15/15</p>
                <div class="color-contener">
                    <a @click="WrongAnswer()"><img src="/src/assets/10.png" alt="interface ui-ux" class="ui-riddle"></a>
                    <a @click="RightAnswer()"><img src="/src/assets/9.png" alt="interface ui-ux" class="ui-riddle"></a>
                </div>
                <p>Quelle est la bonne interface ui ?</p>
            </div>
            <div class="riddle-content">
                <p class="font-purple">2</p>
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

    .logo-riddle {
        width: 100px;
        height: 100px;
        object-fit: contain;
    }

    .ui-riddle {
        width: 150px;
        object-fit: contain;
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

    .font-purple {
        font-size: 100px;
        color: #A24C97;
    }

</style>