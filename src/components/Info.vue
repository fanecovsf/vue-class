<template>
    <div>
        <p v-if="isWorking">Estou trabalhando</p>
        <p v-else>Não estou trabalhando atualmente</p>
        <p>Utilizo as seguintes tecnologias para backend:</p>
        <ul>
            <li v-for="(tec, index) in backendTecs" v-bind:key="index">{{ tec }}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para frontend:</p>
        <ul>
            <li v-for="tec in frontendTecs" v-bind:key="tec.id">{{ tec.name }}</li>
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
            toggleText: 'Esconder email',
            backendTecs: [
                'Python',
                'Java',
                'PHP'
            ],
            frontendTecs: [
                {
                    "id": 1,
                    "name": "Vue.Js",
                },
                {
                    "id": 2,
                    "name": "React.Js"
                }
            ]
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
