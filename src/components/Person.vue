<template>
    <div>
        <h2>Essa pessoa é {{ name }}</h2>
        <p>Estou trabalhando no momento</p>
        <Info/>
    </div>
</template>

<script>
import Info from './Info.vue'

export default {
    name: 'Person',
    data() {
        return {
            name: 'Vinicius'
        }
    },
    
    components: {
        Info
    }
}
</script>
