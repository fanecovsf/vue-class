<template>
    <div>
        <button @click="first(txt1, $event), second(txt2, $event), third($event)">Ativar múltiplos eventos</button>
        <p>{{ multipleEvents }}</p>
        <ReuseVue/>
    </div>
</template>

<script>
    import ReuseVue from './Reuse.vue'

    export default {
        name: 'MultipleEvents',
        data() {
            return {
                multipleEvents: "",
                txt1: "Primeiro evento ativado!",
                txt2: "Segundo evento ativado!"
            }
        },

        methods: {
            async first(txt, e) {
                this.multipleEvents = txt
            },

            async second(txt, e) {
                setTimeout(() => 
                    this.multipleEvents = txt,
                    5000
                )
            },

            async third(e) {
                setTimeout(() => this.multipleEvents = "", 8000)
            }
        },

        components: {
            ReuseVue
        }
    }
</script>

<style scoped>
    div {
        margin: 100px
    }
</style>
