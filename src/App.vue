<template>
  <div class="memories-container">
    <MyHeader appName="#Our Memories"/> 
    <MemoriesList :memories=memories />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MemoriesList from './components/MemoriesList.vue'


export default{
  name: 'App',

  components:{
    MyHeader,
    MemoriesList
  },
  data(){
    return {
      memories: []
    }
  },
  methods:{
    async fetchMemories(){
      const res = await fetch('https://ourmemories-node.onrender.com/api');
      const data = await res.json();
      return data.OurMemories
    }
  },
  async created(){
      this.memories = await this.fetchMemories();
  }
}
</script>


<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}



.memories-container {
    background-color: #b6666f;
    color: black;
    padding: 1em;
}
@media screen and (max-width: 476px) {
  .memories-container {
        width: 100%;
    }
}
</style>
