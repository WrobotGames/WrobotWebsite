<template>
<div> 
    <img class="headerimg" src="/banner.avif" alt="Header Image">
    <div class= "headerbox">
        <header class="header">
            <h2 class="title">Wrobot</h2>
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
                    <a href="/godot">Godot</a>
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


    .headerimg {
        object-fit: cover;
        display: block;
        margin: 0px;
        margin-bottom: 1rem;
        width: 100%;
        height: 200px;
    }
    .headerbox {
        z-index: 999;
        position: fixed;
        background: rgba(255, 255, 255, 0.9);
        top: 0.75rem;
        left: 0.75rem;
        right: 0.75rem;
        border-radius: 15px;
        box-shadow: 0 3px 10px rgba(0,0,0,0.15), 0 1px 4px rgba(0,0,0,0.24);
    }
    .header {
        list-style: none;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0.5rem;
        padding-bottom: 0rem;
    }
    .header .title {
        font-size: 2rem;
        line-height: 0.1rem;
        margin-top: 1rem;
        font-weight: 900;
        color: var(--primary);
    }
    .headerlink {
        margin: 0;
        padding: 0;
        list-style: none;
        display: flex;
        align-items: center;
    }
    .header a {
        text-decoration: none;
        transition: all 0.2s cubic-bezier(.24,.07,.27,1);
        border-radius: 10px;
        text-align: center;
        line-height: 30px;
        list-style: none;
        display: inline-block;
        background: var(--primary);
        color: #fff;
        padding: 0.3rem 1rem;
        margin-left: 0.5rem;
        box-shadow: 0 1px 1px 0px rgba(0, 0, 0, 0.5);
    }
    .header a:hover {
        box-shadow: 0 5px 5px 1px rgba(0, 0, 0, 0.398);
    }
    .header ul{
        margin:0px;
        padding:0px;
    }


    
    @media (max-width:530px) {
        .header{ 
            flex-direction: column;
            
        }
        .header a{
            margin-left: 0.25rem;
            margin-right: 0.25rem;
            padding: 0.25rem 0.75rem;
        }
    }

</style>