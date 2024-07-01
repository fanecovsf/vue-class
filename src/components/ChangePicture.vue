<template>
    <div>
        <button @click="$emit('changePicture')">Trocar imagem</button>
    </div>
</template>

<script>
export default {
    name: 'ChangePicture',

    emits: ['changePicture']
}
</script>

