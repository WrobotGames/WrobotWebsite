<template>
  <div class="pagecontent">
    <h1>About Wrobot.ga</h1>
    <p>I made this website to test making a website with NuxtJS (Vue JS)</p>
    <p>Oh boy the web is a wild place :)</p>
  </div>
</template>

<script>
export default {
 head(){
    return {
        title: 'About the Website - Wrobot',
        meta: [
            {
                hid: 'description',
                name: 'description',
                content: 'A short about on my website, there really isnt anything here.'
            }
        ]
    }
 }
}
</script>

<style>

</style>