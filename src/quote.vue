<template>
    <div>
        <h2 v-for="(i,j) in quotes" :key="j">{{i}}</h2>
    </div>
</template>

<script>
export default {
    props:["quotes"]
}
</script>

<style scoped>
    h2{
        text-align: center;
        background-color: cyan;
        padding: 3rem;
        margin: 4rem;
    }
</style>>