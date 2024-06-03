<template>
   <div>
    <h1>Componentes</h1>
    <p>Meu nome é {{nome}} e minha profissao é {{profissao}}</p>
    <MultiplosEventos/>
    <Reutilizacao/>
    <Reutilizacao/>
    <Reutilizacao/>
    <Reutilizacao/>
    <Reutilizacao/>
    <hr>
   </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue'
    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data() {
            return {
                nome: "Matheus",
                profissao: "Programador"
            }
        }
    }
</script>