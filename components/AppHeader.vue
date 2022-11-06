<template>
<div class= "headerbox">
    <img class="nasa" src="/fog.jpg" alt="Image from space">
  <header class="header">
    <h1 class="title">Wrobot.ga</h1>
    <ul>
        <li>
            <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
            <nuxt-link to="/jokes">Bad Jokes</nuxt-link>
        </li>
        <li>
            <nuxt-link to="/about">About</nuxt-link>
        </li>
        <li>
            <a href="https://wrobot.ga/godot">Godot</a>
        </li>
    </ul>
  </header>
</div>
</template>

<script>
export default {
    name: 'AppHeader'

}
</script>

<style>
    .nasa {
        object-fit: cover;
        display: block;
        margin-left: auto;
        margin-right: auto;
        width: 100%;
        height: 50px;
        border-top-left-radius: 15px;
        border-top-right-radius: 15px;
    }
    .headerbox {
        background: white;
        border-radius: 15px;
        box-shadow: 0 3px 10px rgba(0,0,0,0.15), 0 1px 4px rgba(0,0,0,0.24);
        margin-bottom: 1rem;
    }
    .header {
        list-style: none;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 1rem;
    }
    .header .title {
        margin: 0;
        color: #526488;
    }
    .header ul {
        margin: 0;
        list-style: none;
        display: flex;
        align-items: center;
    }
    .header a {
        font-family: Arial, Helvetica, sans-serif;
        text-decoration: none;
        transition: all 0.4s cubic-bezier(.24,.07,.27,1);
        border-radius: 10px;
        text-align: center;
        line-height: 30px;
        list-style: none;
        display: inline-block;
        background: #526488;
        color: #fff;
        padding: 0.3rem 1rem;
        margin-left: 0.5rem;
    }
    .header a:hover {
        
        background: #6b82b0;
        box-shadow: 0 5px 5px rgba(0,0,0,0.2);
    }


</style>