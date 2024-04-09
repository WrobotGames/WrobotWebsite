<template>
  <main>
    <div class="pagecontent">
        <h1>The Bad Dad Joke List</h1>
        <p >This page has been made to test how api's work. It has been here since 2022, and I dont think I'm going to remove it.</p>
    </div>
    
    <joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke"/>
  </main>
</template>

<script>
import Joke from '../../components/Joke'
export default {
  components: { Joke },
    data(){
        return{
            jokes: []

        }
    },
    async created(){
        const config = {
            headers: {
                'Accept': 'application/json'
            }
        }
        try{
        const res = await useFetch("https://icanhazdadjoke.com/search", {
            headers: {'Accept': 'application/json'}
        });

        this.jokes = res.data._rawValue.results
        }catch(err){
            console.log(err);
        }

    }
}
</script>

<script setup>
useHead({
  title: 'Bad Dad Jokes - Wrobot',
  meta: [{
    name: 'description',
    content: 'If you are seeing this, maybe I should have typed something here.'
  }]
})
</script>

<style>

</style>