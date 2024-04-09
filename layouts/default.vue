<template>
  <div >
    <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400..700;1,400..700&family=Rubik:ital,wght@0,300..900;1,300..900&display=swap" rel="stylesheet">
    <AppHeader/>
    <slot />
    <footer class="pagecontent">
      <h3>You have reached the end!</h3>
      <p>I'm always open for DM's on Mastodon, and you can mail me at contact@wrobot.nl.eu.org.</p>
      <ul class="buttonlist">
        <li><a rel="me" href="https://wrobot.itch.io" class="button">My Itch</a></li>
        <li><a rel="me" href="https://mastodon.gamedev.place/@Wrobot" class="button">My Mastodon</a></li>
        <li><a rel="me" href="https://github.com/WrobotGames" class="button">My Github</a></li>
        <li><a rel="me" href="https://twitter.com/wrobot123" class="button">My Twitter</a></li>
      </ul>
    </footer>
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader';
export default {
    components: {
        AppHeader
    }

}
</script>

<style>
  :root{
    --primary: #224599;
    --secondary: #FF6B35;
    --tertiary: #2fbf71;
    background: rgb(243, 244, 246);
  }
  body{
    margin: 0;
  }
  p{
    font-family: "rubik", sans-serif;
    font-weight: 400;
    color: rgb(54, 54, 54);
  }
  li{
    font-family: "rubik", sans-serif;
    font-weight: 400;
    color: rgb(54, 54, 54);
    padding-bottom: 0.5rem;
  }
  h1, h2, h3, h4, h5, h6, a{
    font-family: "rubik", sans-serif;
    font-weight: 700;
    color: rgb(54, 54, 54);
  }
  h1 {
    color: var(--primary);
    font-family: "rubik", sans-serif;
    font-weight: 900;
    padding-left: 0.0rem;
  }
  .button {
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
        margin-right: 0.5rem;
        box-shadow: 0 1px 2px 0px rgba(0, 0, 0, 0.5);
    }
  .button:hover {
      box-shadow: 0 5px 5px 1px rgba(0, 0, 0, 0.398);
  }
  .buttonlist {
        margin: 0;
        padding: 0;
        list-style: none;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
    }
  .center {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .pagecontent {
    border-radius: 15px;
    margin-bottom: 1rem;
    padding: 1rem;
    margin-left: 15%;
    margin-right: 15%;
    background: white;
    border: 1px solid rgb(232, 232, 232);
    
}
  @media screen and (max-width: 800px) {
    .pagecontent{
      width: calc(100% - 4rem);
      margin-inline: 0;
      padding-inline: 2rem;
      border-left: 0px;
      border-right: 0px;
      border-radius: 0px;
    }
    
  }

/* Page Transitions */
.page-enter-active,
.page-leave-active {
  transition: opacity 0.3s, transform 0.3s;
}

.page-leave-to{
  transform: scale(1.05, 1);
  opacity: 0;
}
.page-enter-from {
  transform: scale(0.95, 1);
  opacity: 0;
}
</style>