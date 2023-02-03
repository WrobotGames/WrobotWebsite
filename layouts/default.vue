<template>
  <div >
    <AppHeader/>
    <slot />
    <footer class="pagecontent">
      <h3>You have reached the end!</h3>
      <p>This may be the end of this page, but this shouldn't be the end of 'Looking at random stuff I made', so I really recommend looking at my Mastodon page.</p>
      <a rel="me" href="https://mastodon.gamedev.place/@Wrobot" class="mastodon">My Mastodon</a>
      <p>If you have any questions or suggestions, I'm always open for DM's on Mastodon</p>
      <p>I have twitter too, but I'm not active there. @Wrobot123</p>
      <a rel="me" href="https://github.com/WrobotGames" class="mastodon">My Github</a>
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
    --primary: #54749f;
    background: rgb(243, 244, 246);
  }
  body{
    margin: 0;
  }
  p, h1, h2, h3, h4, h5, h6, a{
    font-family: Arial, Helvetica, sans-serif;
    color: rgb(54, 54, 54);
  }
  h1 {
    border-left: 3px solid var(--primary);
    padding-left: 0.5rem;
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

.mastodon {
  display: block;
  width: 10rem;
  border: 0;
  border-radius: 7px;
  background: #595aff;
  color: #fff;
  font-size: 18px;
  line-height: inherit;
  height: auto;
  padding: 10px;
  text-decoration: none;
  text-align: center;
  box-sizing: border-box;
  cursor: pointer;
  font-weight: 500;
  outline: 0;
  margin-bottom: 10px;
  margin-right: 10px;
}


</style>