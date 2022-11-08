<template>
<div> 
    <img class="nasa" src="/fog.jpg" alt="Image from space">
    <div class= "headerbox">
        <header class="header">
            <h1 class="title">Wrobot</h1>
            <!--<button class="mobile_toggle" @click="togglemenu"></button>-->
            <ul class="headerlink">
                <li>
                    <nuxt-link to="/">Home</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/jokes">Jokes</nuxt-link>
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
</div>
</template>

<script>
import { ref } from 'vue'
export default {
    name: 'AppHeader'

}
const is_expanded = ref(false)
const togglemenu = () => {
    is_expanded.value = !is_expanded.value

}
</script>

<style>


    .nasa {
        object-fit: cover;
        display: block;
        margin-left: -8px;
        margin-top: -8px;
        margin-right: -8px;
        margin-bottom: 1rem;
        width: calc(100% + 16px);
        height: 158px;
    }
    .headerbox {
        z-index: 999;
        width: calc(100% - 16px );
        position: fixed;
        background: rgba(255, 255, 255, 0.8);
        top: 1rem;
        border-radius: 15px;
        box-shadow: 0 3px 10px rgba(0,0,0,0.15), 0 1px 4px rgba(0,0,0,0.24);
        backdrop-filter: blur(1rem);
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
    .headerlink {
        margin: 0;
        padding: 0;
        list-style: none;
        display: flex;
        align-items: center;
    }
    .mobile_toggle{
        display: none;
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
    @media (max-width:500px) {
        .header{ 
            flex-direction: column;
            align-items: flex-start;
        }
        .headerlink{
            padding: 0;
            flex-wrap:nowrap;
            width: 100%;
            margin-top: 0.5rem;
            justify-content: space-between;

        }

        .headerlink a {
            box-shadow: 0 3px 10px rgba(0,0,0,0.15), 0 1px 4px rgba(0,0,0,0.24);

            max-width: 200px;
            width: 50px;
            margin: 0;
            padding-inline: 0.5rem;
            font-size: 15px;
        }
        
        /*
        .mobile_toggle{
            display: block;
            top: 2rem;
            right: calc(75px - 1rem);
            z-index: 9999999;
            border:0;
            position: absolute;
            background: url(/menu.svg);
            background-repeat: no-repeat;
            background-size: 2rem;
            width:2rem;
            aspect-ratio: 1;
        }*/
        
    }
    


</style>