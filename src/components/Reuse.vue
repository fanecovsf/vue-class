<template>
    <div>
        <button @click="activate">Clique aqui!</button>
        <span v-show="active">Ativado!</span>
    </div>
</template>

<script>
    export default {
        name: 'Reuse',
        
        data() {
            return {
                active: false
            }
        },

        methods: {
            async activate() {
                this.active = !this.active
            }
        }
    }
</script>

<style scoped>
    button {
        margin: 10px
    }
</style>
