<template>
    <div>
        <button @click="primeiro(txt1, $event), segundo(txt2, $event), terceiro()">Ativar mútiplos eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>


<!-- MULTIPLOS EVENTOS: é uma forma de ativar dois ou mais métodos com apenas uma ação do usuário. -->
<script>
    export default {
        name: 'MultiplosEventos',
        data() {
            return {
                multiplos_eventos: "",
                txt1: "Primeiro evento",
                txt2: "Segundo evento"
            }
        },
        methods: {
            primeiro(txt, e) {
                this.multiplos_eventos = txt;
            },
            segundo(txt, e) {
                setTimeout(() => this.multiplos_eventos = txt, 500)
                },
            terceiro() {
                setTimeout(() => this.multiplos_eventos = "", 1500)
                }
            }
        }
</script>