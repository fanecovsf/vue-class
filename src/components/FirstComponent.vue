<template>
    <div>
        <h1>Meu primeiro componente</h1>
        <p>Componente {{name}}</p>
        <p>Idade: {{age}}</p>
    </div>
</template>

<script>
    export default {
        name: 'FirstComponent',
        data() {
            return {
                name: 'Jeunesse',
                age: 3
            }
        }
    }
</script>
