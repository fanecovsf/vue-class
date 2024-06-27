<template>
    <div>
        <h1>Meu primeiro componente</h1>
        <p>Componente {{name}}</p>
        <p>Idade: {{age}}</p>
        <MultipleEventsVue/>
        <ReuseVue/>
        <ReuseVue/>
        <ReuseVue/>
    </div>
</template>

<script>
    import MultipleEventsVue from './MultipleEvents.vue'
    import ReuseVue from './Reuse.vue'

    export default {
        name: 'FirstComponent',
        data() {
            return {
                name: 'Jeunesse',
                age: 3
            }
        },

        components: {
            MultipleEventsVue,
            ReuseVue
        }
    }
</script>
