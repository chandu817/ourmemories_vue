<template>
    <div class="single-memory">
        <img width="250" height="250" :src="memory.Image" alt="">
        <h2 class="memory-occasion">{{ memory.occasion }}</h2>
        <p class="memory-location">{{ memory.location }} | {{ memory.year }}</p>
        <div class="names">
            <div class="name" v-for="name of memory.names" :key="name">
            <p># {{ name }}</p>
        </div>
        </div>

    </div>
</template>

<script>

export default {
    name: 'SingleMemory',
    props: {
        memory: Object
    }
}
</script>

<style scoped>
.single-memory {
    background-color: #fef2f2;
    display: flex;
    flex-direction: column;
    width: 250px;
    text-align: center;
}
.memory-occasion {
    color: #f53163;
    text-align: center;
    margin-top: 0.5em;
    text-transform: capitalize;
}
.names {
    color: #f53163;
    display: flex;
    margin-top: 0.5em;
    justify-content: center;
}
.name {
    margin-right: 10px;
    font-size: 13px;
    font-weight: bold;
}
.memory-location {
    color: #7a77b9;
    margin-top: 0.5em;
    margin-bottom: 0.5em;

}
</style>