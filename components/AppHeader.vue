<template>
<div> 
    <img class="nasa" src="/fog.jpg" alt="Header Image">
    <div class= "headerbox">
        <header class="header">
            <h2 class="title">Wrobot</h2>
            <!--<button class="mobile_toggle" @click="togglemenu"></button>-->
            <ul class="headerlink">
                <li >
                    <h2 class="mobiletext">Menu</h2>
                </li>
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
        margin: 0px;
        margin-bottom: 1rem;
        width: 100%;
        height: 158px;
    }
    .headerbox {
        z-index: 999;
        position: fixed;
        background: rgba(255, 255, 255, 0.7);
        top: 0.75rem;
        left: 0.75rem;
        right: 0.75rem;
        border-radius: 15px;
        box-shadow: 0 3px 10px rgba(0,0,0,0.15), 0 1px 4px rgba(0,0,0,0.24);
        backdrop-filter: blur(0.5rem);
    }
    .header {
        list-style: none;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0.75rem;
    }
    .header .title {
        font-size: 2rem;
        margin: 0;
        color: var(--primary);
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
        background: var(--primary);
        color: #fff;
        padding: 0.3rem 1rem;
        margin-left: 0.5rem;
    }
    .header a:hover {
        color: var(--primary);
        background: #ffffff;
        box-shadow: 0 0px 5px 5px rgba(0, 0, 0, 0.1);
    }
    .mobiletext{
        display: none;
    }


    
    @media (max-width:500px) {
        .header{ 
            flex-direction: column;
            align-items: flex-start;
        }
        .headerlink{
            flex-direction: column;
            justify-content: flex-start;
                position: fixed;
                right: -0.75rem;
                top: 0;
                padding: 0;
                width:200px;
                height: calc(100vh - 1.5rem);
                background: rgba(256, 256, 256, 0.742);
                backdrop-filter: blur(10px);
                border-top-left-radius: 15px;
                border-bottom-left-radius: 15px;
                box-shadow: 0 3px 10px rgba(0,0,0,0.15), 0 1px 4px rgba(0,0,0,0.24);

        }

        .headerlink a {
            box-shadow: 0 3px 10px rgba(0,0,0,0.15), 0 1px 4px rgba(0,0,0,0.24);
            width: calc(200px - 2rem);
            padding: 0;
            padding-top: 0.5rem;
            padding-bottom: 0.5rem;
            margin: 0;
            margin-top: 1rem;
        }
        .mobiletext{
            text-align: center;
            width: calc(200px - 2rem);
            display: block;
            margin: 0;
            margin-top: 1rem;
            padding: 0;
            height: auto;
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