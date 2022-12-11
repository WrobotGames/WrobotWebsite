<template>
  <div >
    <AppHeader/>
    <slot />
    <footer class="pagecontent">
      <h3>You have reached the end!</h3>
      <p>This is such a cool footer, I wonder why there inst anything here.</p>
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
  p, h1, h2, h3, h4, h5, h6{
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

</style>