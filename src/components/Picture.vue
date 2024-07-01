<template>
    <img v-show="showDash" :src="dash" alt="">
    <ChangePictureVue @changePicture="changePic"/>
</template>

<script>
import ChangePictureVue from './ChangePicture'

export default {
    // v-bind pode ser resumido apenas com 2 pontos
    // path iniciando com / sempre vai apontar para a pasta public do projeto
    name: 'Picture',
    data() {
        return {
            dash: '/img/dash.png',
            showDash: true
        }
    },

    components: {
        ChangePictureVue
    },

    methods: {
        changePic() {
            if (this.dash == '/img/dash.png') {
                this.dash = '/img/dash2.png'
            } else {
                this.dash = '/img/dash.png'
            }
        }
    }
}
</script>