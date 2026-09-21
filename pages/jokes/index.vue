<template>
  <main>
    <div class="pagecontent">
        <h1>The Bad Dad Joke List</h1>
        <p >This page has been made to test how api's work, and to experiment a little bit with CSS. It has been here since 2022, and I dont think I'm going to remove it. I mean, why would I? Who doesn't like some really bad jokes.</p>
    </div>
    
    <joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke"/>
  </main>
</template>

<script setup>
import Joke from '../../components/Joke.vue'
useHead({
  title: 'Bad Dad Jokes - Wrobot',
  meta: [{
    name: 'description',
    content: 'If you are seeing this, maybe I should have typed something here.'
  }]
})
const { data } = await useFetch('https://icanhazdadjoke.com/search', {
  headers: { 'Accept': 'application/json' }
})

// Safely extract the joke list
const jokes = computed(() => data.value?.results || [])
</script>

<style>

</style>