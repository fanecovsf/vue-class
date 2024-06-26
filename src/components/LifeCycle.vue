<template>
    <div>
        <h1>Meu nome é: {{ name }}</h1>
    </div>
</template>

<script>
    export default {
        name: 'LifeCycle',

        data() {
            return {
                name: 'To em dúvida'
            }
        },

        created() {
            setTimeout(() => {
                this.name = 'Gustavo'
            }, 1000)
        },

        mounted() {
            setTimeout(() => {
                this.name = 'Felipe'
            }, 2000)
        }
    }
</script>
