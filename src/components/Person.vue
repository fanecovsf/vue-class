<template>
    <div>
        <h2>Essa pessoa é {{ name }}</h2>
        <Info :email="email"/>
    </div>
</template>

<script>
import Info from './Info.vue'

export default {
    name: 'Person',
    data() {
        return {
            name: 'Vinicius',
            email: 'props@email.com'
        }
    },
    
    components: {
        Info
    }
}
</script>
