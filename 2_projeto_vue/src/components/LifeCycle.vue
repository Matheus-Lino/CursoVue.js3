<template>
    <div>
        <h1>LifeCycle Hooks</h1>
        <h2>Meu nome é: {{ nome }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'LifeCycle',
        data() {
            return {
                nome: "Ainda não sei"
            }
        },
        created() {
            setTimeout (() => {  
                this.nome = "Matheus"
            }, 1000)
            this.LifeCycle()
        } ,
        mounted() {
            setTimeout (() => {
                this.nome = "Pedro"
            }, 2000)
            this.LifeCycle()
        },
        methods: {
            LifeCycle() {
                console.log("Executou")
            }
        }
    }
</script>

