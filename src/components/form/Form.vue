<template>
    <div>
        <form action="" @submit="sendForm($event)">
            <input type="text" v-model="name">
            <input type="text" v-model="email">
            <InputSubmitVue/>
        </form>
    </div>
</template>

<script>
import InputSubmitVue from './InputSubmit.vue'
import InputTextVue from './InputText.vue'

export default {
    name: 'Form',
    components: {
        InputSubmitVue,
        InputTextVue
    },

    methods: {
        async sendForm(e) {
            e.preventDefault()

            const name = this.name
            const email = this.email
        }
    },

    data() {
        return {
            name: '',
            email: ''
        }
    }
}
</script>

<style scoped>
    div {
        display: flex;
        justify-content: center;
        align-items: center
    }

    form {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center
    }

    form input {
        margin: 5px
    }
</style>
