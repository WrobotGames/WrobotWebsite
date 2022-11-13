<template>
  <div>
    <div class="pagecontent">
        <h1>The Bad Dad Joke List</h1>
        <p >Here is a list of bad jokes, just to test on how to make a website.</p>
    </div>
    
    <joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke"/>
  </div>
</template>

<script>
import axios from 'axios';
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

        
        const res = await axios.get('https://icanhazdadjoke.com/search', config);
        this.jokes = res.data.results;
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