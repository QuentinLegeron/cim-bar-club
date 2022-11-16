<template>
    <section>
        <a href="#/"><img src="/src/assets/Logo.png" alt="logo crea" style="width: 100px"></a>
        <p @click="MyFunction()">enter la réponse</p>
        <!-- <p>Post it "F12"</p>
        <p>Post it -> console</p> -->
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
                console.log('\n \n \n \nIndice :\n En informatique , il bug au moindre problème.\n il ne mesure que 4 lettres.\n \n \n \n')
            }
        },

        MyFunction() {
        let answer = prompt("Quelle est la réponse à l'énigme?", '')
        this.ConsoleLogEnigma(answer)
        }
    },

    mounted() {
        this.ConsoleLogEnigma(null)
    },
}

</script>

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

</style>