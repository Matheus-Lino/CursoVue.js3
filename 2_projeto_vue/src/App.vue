<template>
    <div>
        <Header :esta_logado="true"/>
        <primeiro-componente/>
        <p class="paragrafo-pai"> O dado do app é: {{ testando }}</p>
        <hr>
        <LifeCycle/>
        <pessoa/>
    </div>
</template>

<script>
    import PrimeiroComponente from './components/primeiroComponente.vue'
    import LifeCycle from './components/LifeCycle.vue'
    import Pessoa from './components/Pessoa.vue'
    import Form from './components/Form.vue'
    import Header from './components/Header.vue'

    export default {
        name: 'App',
        components: {
            PrimeiroComponente,
            LifeCycle,
            Pessoa,
            Form,
            Header
        },
        data() {
            return {
                testando: "Teste"
            }
        }
    }
</script>

<!--CSS global (para toda a aplicação) -->
<style>
    body {
        background-color: #333;
        color: white;
    }

    a {
        color: red;
    }
</style>