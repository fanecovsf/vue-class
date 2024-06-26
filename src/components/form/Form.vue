<template>
    <div>
        <form action="">
            <InputTextVue/>
            <InputTextVue/>
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
    }
}
</script>