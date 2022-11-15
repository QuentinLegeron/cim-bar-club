<template>
    <section>
        <a href="#/">Index</a>
        <a href=""></a>
        <h1>Window 10</h1>
        <p @click="MyFunction()">enter la réponse</p>
        <p>Post it "F12"</p>
        <p>Post it -> console</p>
    </section>
</template>

<script lang="ts">

export default {
    name: 'DevWeb',

    methods: {
        ConsoleLogEnigma(answer: string | null) {
            const reponse = 'code'
            if (answer === reponse) {
                console.log("Bien joué !\n \n La clef de l'axe dev web est un 4 noir.\n \n n'oublie pas de le noter pour pas l'oublier.")
                return
            }
            console.log("\n \n \nC'est un civil à respecter.\n Souvent gardien de nos entrées.\n Sur la route, il est suivi.\n En génétique, il nous définit.\n Qui est-il ?\n \n \n")
            if (answer === null) {
                console.log("entre une reponse en appuyant sur le bouton pour avoir la clef de l'axe dev")
            }
            else{
                console.log('Indice :\n Il bug au moindre problème.\n il ne mesure que 4 lettres.')
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