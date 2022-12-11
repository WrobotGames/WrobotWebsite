<template>
  <main>
    <div class="pagecontent">
        <h1>The Bad Dad Joke List</h1>
        <p >This is me testing website API's, it seems to work well.</p>
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

        console.log(useFetch("https://icanhazdadjoke.com/search", {
            headers: {'Accept': 'application/json'}
        }).data._rawValue.results)
        this.jokes = useFetch("https://icanhazdadjoke.com/search", {
            headers: {'Accept': 'application/json'}
        }).data._rawValue.results
        }catch(err){
            console.log(err);
        }

    },
    head(){
        return {
            title: 'Dad Jokes - Wrobot',
            meta: [
                {
                    hid: 'description',
                    name: 'description',
                    content: 'Here is a list of bad dad jokes, just to test on how to make a website.'
                }
            ]
        }
 }
}
</script>

<style>

</style>