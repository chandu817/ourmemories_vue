<template>
    <div class="memories-list">
        <div class="memories" v-for="memory of memories" :key="memory.id">
            <SingleMemory :memory=memory />
        </div>
    </div>
</template>
<script>
import SingleMemory from './SingleMemory.vue'

export default {
    name: 'MemoryList',
    props: {
        memories: Array
    },
    components: {
        SingleMemory
    }

}
</script>
<style scoped>
.memories-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
}
.memories {
    margin: 1em;
    background-color: #fff;
    padding: 1em;

}
</style>
