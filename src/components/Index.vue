<template>
    <section>
        <h1>Bonjour.</h1>
        <p @click="MyFunction()">enter la réponse</p>
        <p>Post it "F12"</p>
    </section>
</template>

<script lang="ts">

export default {
    name: 'Index',


    methods: {
        ConsoleLogEnigma(answer: string | null) {
            const reponse = 'code'
            if (answer === reponse) {
                console.log("Bien joué !\n \n La clef de l'axe dev web est un 4 rouge.\n \n n'oublie pas de le noter pour pas l'oublier.")
                return
            }
            console.log("\n \n \nC'est un civil à respecter.\n Souvent gardien de nos entrées.\n Sur la route, il est suivi.\n En générique, il définit.\n Qui est-il ?\n \n \n")
            if (answer === null) {
                console.log("entre une reponse en appuyant sur le bouton pour avoir la clef de l'axe dev")
            }
            else{
                console.log('Indice :\n Il bug au moindre problème.')
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