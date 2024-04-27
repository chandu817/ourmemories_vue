<template>
    <div class="header">
        <h1> {{ appName }} </h1>
    </div>
</template>

<script>
export default {
    name: 'MyHeader',
    props: {
        appName: String,
    }
}
</script>

<style scoped>
.header {
    text-align: center;
    padding: 1em 0;
    background-color: black;
    color: #ff007f;
}
</style>