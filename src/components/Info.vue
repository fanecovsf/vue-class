<template>
    <div>
        <p v-if="isWorking">Estou trabalhando</p>
        <p v-else>Não estou trabalhando atualmente</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>Javascript</li>
            <li>Node.Js</li>
        </ul>
        <p v-show="showEmail">Mande uma mensagem para: {{ email }}</p>
    </div>
</template>

<script>
export default {
    name: 'Info',
    data() {
        return {
            isWorking: false,
            showEmail: true,
            email: 'teste@teste.com'
        }
    }
}
</script>