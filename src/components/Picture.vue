<template>
    <img v-show="showDash" :src="dash" alt="">
</template>

<script>
export default {
    // v-bind pode ser resumido apenas com 2 pontos
    // path iniciando com / sempre vai apontar para a pasta public do projeto
    name: 'Picture',
    data() {
        return {
            dash: '/img/dash.png',
            showDash: true
        }
    }
}
</script>