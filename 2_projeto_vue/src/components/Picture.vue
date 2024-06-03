<template>
    <div>
        <img :src="avatar" :alt="descricao">
        <MudarImagem @mudar-imagem="TrocarImagem"/>
    </div>
</template>

<script>
import MudarImagem from './MudarImagem.vue';

    export default {
        name: 'Picture',
        components: {
            MudarImagem
        },
        data() {
            return {
                avatar: './img/avatar.png',
                descricao: 'Matheus Lino'
            }
        },
        methods: {
            TrocarImagem() {
                this.avatar = "./img/avatar2.png"
            }
        }
    }
</script>