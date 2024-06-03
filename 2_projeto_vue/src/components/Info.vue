<template>
    <div>
        <p>{{ compEmail }}  {{ email }}</p>
        <hr>
        <h2>Esta é da descrição da pessoa: {{ nome }}</h2>
        <p v-if="esta_Trabalhando">Estou trabalhando no momento</p>
        <p v-else> Estou em busca de novas oportunidades</p>
        <div>
            <button  @click="ShowEmail">{{ textoBotao }}</button>
        </div>
        <p v-show="mostrar_Email">Mandar email para {{email}}</p>
        <p>Uso as seguintes tecnologias</p>
        <p>Para acessar meu portifolio<a :href="meu_link" target="_blank">CliqueAqui</a></p>
        <Picture/>
        <!-- aprender a renderizar listas, ou seja, imprimir arrays no HTML com #Vue, vamos utilizar uma diretiva bem famosa: a v-for, que faz um loop em um array, que pode também ser um array de objetos. -->
        <ul>
            <li v-for="(tecnologias, index) in backend_technologies" v-bind:key="index">{{ tecnologias }}</li>
        </ul>
        <p>Ultilizo as seguintes linguagens para Front-End</p>
        <ul>
            <li v-for="tecnologias in frontend_technologies" :key="tecnologias.id">{{ tecnologias.language }}</li>
        </ul>
    </div>
</template>

<script>
    import Picture from './Picture.vue'
    export default {
        name: 'Info',
        components: {
            Picture

        },
        props: {
            email: String,
            esta_Trabalhando: Boolean
        },
        data() {
            return {
                mostrar_Email: false,
                meu_link: 'https://google.com',
                textoBotao: 'Mostrar Email',
                backend_technologies: ['JavaScript', 'PHP', 'Python'],
                frontend_technologies: [
                    {id: 1, language: "HTML"},
                    {id: 2, language: "CSS"},
                    {id: 3, language: "JAVASCRIPT"}
                ]
            }
        },
        methods: {
            ShowEmail() {
                this.mostrar_Email = !this.mostrar_Email
                if (!this.mostrar_Email) {
                    this.textoBotao = "Enviar Email"
                } else {
                    this.textoBotao = "Esconder Botão"
                }
            }
        }
    }
</script>
<style>
    .paragrafo-pai {
        color: red;
    }
</style>