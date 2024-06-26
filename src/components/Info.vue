<template>
    <div>
        <p v-if="isWorking">Estou trabalhando</p>
        <p v-else>Não estou trabalhando atualmente</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>Javascript</li>
            <li>Node.Js</li>
        </ul>
        <div>
            <button @click="toggleEmail">{{ toggleText }}</button>
        </div>
        <p v-show="showEmail">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portifólio, clique <a v-bind:href="portLink" target="_blank">aqui</a></p>
    </div>
</template>

<script>
export default {
    name: 'Info',
    data() {
        return {
            isWorking: false,
            showEmail: true,
            email: 'teste@teste.com',
            portLink: 'https://google.com',
            toggleText: 'Esconder email'
        }
    },

    methods: {
        async toggleEmail() {
            this.showEmail = !this.showEmail
            if (this.toggleText == 'Esconder email') {
                this.toggleText = 'Mostrar botão'
            } else {
                this.toggleText = 'Esconder email'
            }
        }
    }
}
</script>

<style>
    a {
        color: white;
    }
</style>
