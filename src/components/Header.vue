<template>
    <div>
        <ul>
            <li :headerList="headherList" v-for="(header, index) in headerList" :key="index"><a href="">{{ header }}</a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Header',

    props: {
        headerList: Array
    }
}
</script>

<style scoped>
    div {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: blue;
    }

    div ul {
        display: flex;
        justify-content: space-between;
        padding: 10px;
    }

    li {
        margin: 10px
    }

    a {
        margin: 3px;
        color: white;
    }

    a:hover {
        color: brown;
        transition: 0.3s ease-in;
    }
</style>

